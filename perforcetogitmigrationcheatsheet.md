## Perforce to Git: Best Practices
There is a lot to account for when considering or planning a change from Perforce to Git. To ensure a healthy, happy move, we recommend a tiered approach:
- [Assess current workflow and estimate toolchain impact](#assess-current-workflow-and-estimate-toolchain-impact)
- [Determine what to migrate](#determine-what-to-migrate)
- [Preliminary steps and preparations](#preliminary-steps-and-preparations)
- [Migrate source code](#migrate-source-code)
- [Revisit workflow to measure progress](#revisit-workflow-to-measure-progress)

### Assess current workflow and estimate toolchain impact
Migrating to GitHub is more than just moving source code. A successful migration includes a planned effort around cultural transformation, workflow modernization, and improved collaboration. It's important to:
- Set expectations
  - Decide how and when you'll switch to Git. This could be gradually (by team or repository), or in a single organization-wide move.
  - Determine how much history _actually_ needs to be migrated to Git. 
    - Migrating history actually means _re-creating_ that history via new commits, so be aware that this new history may not meet audit or compliance requirements.
    - Commit history for a default (trunk) branch/codeline may be more useful than the more ephemeral branches used during development. Many teams opt to migrate the history of just their default branch when switching between version control systems.
- Determine changes to workflow
  - How will you adapt workflows to take full advantage of Git's distributed nature?
  - Do your current repositories exhibit qualities that can negatively impact Git performance? These can include large binaries, a monolithic multi-project structure, and long-running or divergent branches.
  - How will you communicate these recommended workflow changes to your teams?
  - What other tools in your current workflow (build systems, CI, deployment) will be impacted by the change to Git?
- Enable everyone with training
  - Provide training so that your developer teams are comfortable and confident with Git and GitHub. This provides a positive experience for developers, avoids misconceptions, and eliminates confusion.
  - Document and collaborate on your updated workflows in a shared space.

#### How Git is different
Going hand-in-hand with the cultural shift, you need to be aware of how using Git differs:
- Forks and Remotes mean you can push code to different locations
- SHA hashes identify individual commits
- Git/GitHub use a Staging Area
- Workflows will need to adapt 
  - Branches are easy to make and are intended to be emphemeral (merged back into a default/`master` branch when ready).
  - Pull Requests are used to have conversations and collaborate, then are merged when ready.
  - The GitHub UI is very user-friendly, but can take some adjustment, particularly for teams not used to communicating & collaborating in writing.

#### Pre-migration considerations
Before you migrate, it is ideal to stop working in Perforce until you perform the migration, and then switch completely to Git. This avoids "drift" where code changes could occur in multiple authoritative locations.
  - If this isn't possible, utilize `cron` jobs to update repositories every week.
  - If your developers aren't comfortable making a clean switch to Git, having their source code in both will allow them to work towards Git and allow them to report issues up front, and then when they are comfortable you can place Perforce repositories in read-only mode.
  - It's a good idea to have Git and GitHub subject matter experts to whom team members can address their questions and concerns.
  - Having a wiki or README with basic information or a Q&A can be helpful.
  - Training is always helpful and increases comfort levels and confidence.
  - Knowledge will start to transfer organically, but can be accelerated by shared spaces for information exchange.

### Determine what to migrate
#### The challenge
The biggest challenge when migrating from Perforce to Git is preserving large histories. Other issues to consider include dependencies and superflous branches.

#### The solution
1. Do you even need to bring over a full history? If you can place everything into read-only mode and leave it in Perforce, this is the simplest solution.
  - Scrutinize what, if any, files should be migrated and be highly selective.

2. If you're unable to leave everything in Perforce and start fresh in Git, determine what the essential items are, and omit transferring anything non-essential.
  - Can you initialize with your current working tree?
  - Can you bring over a single branch and move forward from there?
  - Determine methods for bringing over branches and history that represent the essential, minimal amount of information you need.

3. Examine the size of the source repository. While there is no real "cut off" regarding the size, a good sanity-check point would be to try to keep repositories under 1GB.
  - If a repository is over 1GB in size, can you determine why? Are there large binaries or compiled binary artifacts checked into version control?
    - These binary artifacts could be moved into [Releases](https://help.github.com/articles/about-releases/) or [Git LFS](https://git-lfs.github.com/), as appropriate.
  - Is the repository monolithic, combining several related projects together? Could it be separated into smaller component repositories?

4. Take the time to clean up and restructure repositories before migrating to alleviate time, confusion, and clean-up post-migration. Branch history can get complicated and may not line up with how Git thinks about things. 
  - Restructuring after the fact can a bigger undertaking than doing this step in advance.
  - Do you need to bring over all branches?
    
### Preliminary steps and preparations
We stress and suggest the following steps to ensure all neccessary items transfer into Git. Non-essential items, such as superflous branches, should be removed before the actual process of migration.

1. If possible, go through and remove any collateral that isn't vital to keep and transfer; try to reduce the number of files in your repositories.
  - Doing this will minimize migration time and chance of error
  - Often times there can be numerous branches that have been merged, and can be deleted
  - Doing this enables your "fresh start" in Git to be as clean as possible, allowing focus on the items of actual importance that are allowed to remain
  - If you have more than 100,000 files, you may need to extract components, which will likely require refactoring. This makes sense for independent components that do not share the same "pace of development".

2. Ready your environment for migration. 
  - Make sure you have Python installed, in order to use `git-p4`
  - Have the latest version of `git-p4` installed. This tool does the heavy lifting for migration.
  - Have Git LFS installed to support large files
  - Ensure that you have at least Git 2.6 installed to avoid issues with case sensitivity

#### Migration timing
- Restructuring repositories is the most time-consuming step
- Running `git-p4` can take a few hours
- The actual migration will be quicker
- Verify your history locally before pushing to GitHub

### Migrate source code
It's a good idea to clone something in Perforce to experiment with before actually migrating so you can:
- See what it looks like
- Determine if the history is understandable
- Ascertain resulting repository sizes

__When you're ready to proceed:__

1. Migrate repositories using `git-p4` (Python tool included with Git - does heavy lifting of moving from Perforce to Git)
```
export P4USER="lars" // set up Perforce and tell what user you should use
export P4PORT="tcp:my-perforce-server.com:12345" // set up Perforce server'

p4 login

mkdir demo && cd demo

git-p4 clone //depot@all . --verbose
// this tells p4 to clone perforce directory and move it to git, then the base part of the perforce repository that we want to migrate, the suffix `all` tells git-p4 to move all history to Git. All changes in Perforce will become Git Commits. 3rd parameter tells you to store resulting git repository right into that directory. And then last parameters (`--verbose`) gives you details on when git-p4 is running. This command will run quite awhile, then the repository will be on your local machine.

git remote add origin git@github.com:org/demo.git

git push origin
```

…and you're done!

#### How to import branches
1. Import Perforce branch directories as individual Git branches, they have no connection at all (e.g. Release and Master branch)
2. Create a copy of your branch (e.g. copy your Release branch: `p4-history/Release`)
3. Squash commits of the release branch into one commit and rename your branch (e.g. Squashed release)
4. Create a new Git branch (Release branch) based on `master`
5. Commit the delta of the squashed branch: Move all changes from the squashed Release branch to the new Release branch

__Note:__ 
An issue with this is history: you can look into the `p4-history/Release` branch for more details since all the changes were squashed into one commit.

### Revisit workflow to measure progress
Cultural transformations do not often happen overnight, so it's vital to have timely check-ins for:
- Developer happiness & productivity
  - Does everyone understand how to use Git and GitHub effectively?
  - Do they know who can answer any questions?
  - Are there any clarifications that need to be made?
- Workflow consistency
  - Is the updated workflow effective?
  - Is the workflow being followed consistently?
  - Are there any adaptations that need to be made?
  - Is the workflow clearly documented for future team members?

### Further resources
- [Lars Schneider's "From Perforce to Git: Lessons Learned" talk at GitHub Universe](https://larsxschneider.github.io/2016/02/03/github-universe-talk)
- [GitHub Professional Services](https://services.github.com/) - we offer help with everything from training and admin mentoring to workflow consultations and cultural transformation packages to help you succeed in your endeavors
