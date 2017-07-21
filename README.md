# GitHub for Developers

- Class Date: July 19 - 20, 2017
- Facilitator:
  - @hollenberry :microphone:

## Scripts for Adding Files

- **Bash:** `for d in {1..6}; do touch file$d.md; git add file$d.md; git commit -m "adding file $d"; done`
- **PowerShell:** `for ($d=1; $d -le 6;$d++) { touch file$d.md; git add file$d.md; git commit -m "adding file$d.md";}`

## Core Resources Used During Class

- [GitHub for Developers Manual](https://github.github.io/training-manual/)
- [Git Cheat Sheets](https://services.github.com/resources/)
- [Review videos - curriculum bites broken into pieces](https://www.youtube.com/playlist?list=PLg7s6cbtAD16Pgp6WIVfX4VsGI-xyWkMz)
- [Introduction to GitHub Flow](https://guides.github.com/introduction/flow/)
- [Authentication Troubleshooting Guide](https://help.github.com/categories/authenticating-to-github/)
- [git-scm](https://git-scm.com)
- [GitSchool - Visualizing Git](http://git-school.github.io/visualizing-git/)
- [LearnGitBranching](http://learngitbranching.js.org/?NODEMO)
- [Raw view of Day 1 CLI History](https://raw.githubusercontent.com/githubschool/ideal-train/master/day1shellhistory.md) -- save this locally in case of deletion
- [Raw view of Day 2 CLI History](https://raw.githubusercontent.com/githubschool/ideal-train/master/day2shellhistory.md) -- save this locally in case of deletion
- [Eric's CLI Z-Shell](https://github.com/sorin-ionescu/prezto)

### Class Images
- [Git Configuration Levels](https://services.github.com/on-demand/images/config-levels.jpg)
- [The Two Stage Commit](https://services.github.com/on-demand/images/two-stage-commit-a.jpg)
- [Reset Modes](https://services.github.com/on-demand/images/reset-modes.jpg)


## Additional Topics

- [Perforce to Git Command Mapping](https://www.perforce.com/perforce/r15.1/manuals/dvcs/_git_perforce_command_mappings.html)
- [Perforce to Git Migration Cheat Sheet](https://github.com/githubschool/ideal-train/blob/master/perforcetogitmigrationcheatsheet.md)
- [2FA and CLI Authentication](https://help.github.com/articles/providing-your-2fa-authentication-code/#through-the-command-line)
- [Atom](https://atom.io/) and [Visual Studio Code](https://code.visualstudio.com/)
- [CLI Navigation Resource](https://services.github.com/on-demand/downloads/github-bash-cheat-sheet/)
- [How to: Code Owners](https://help.github.com/articles/about-codeowners/)
- [Fun Git Aliases](http://haacked.com/archive/2014/07/28/github-flow-aliases/)
- [Working with Submodules](https://github.com/blog/2104-working-with-submodules)
- [Comparing Commits Across Time](https://help.github.com/articles/comparing-commits-across-time/)
- [Why are Git objects subdivided into so many SHA-prefix folders?](https://softwareengineering.stackexchange.com/questions/301400/why-is-the-git-git-objects-folder-subdivided-in-many-sha-prefix-folders)
- [The API for Pull Request Comments](https://developer.github.com/v3/pulls/comments/)
- [Mavensmate Atom Plugin](https://github.com/joeferraro/MavensMate-Atom)
- [Git Hooks](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks) -- This all happens client side
- [Pre-receive hooks](https://help.github.com/enterprise/2.10/admin/guides/developer-workflow/creating-a-pre-receive-hook-script/) -- this happens on the remote
- [gitk](https://git-scm.com/docs/gitk)
- [Listing projects that depend on a repository](https://help.github.com/articles/listing-the-projects-that-depend-on-a-repository/) -- separate from submodules
- [Hub -- A CLI wrapper for Git](https://hub.github.com/) -- this is a tool for creating a PR from the CLI
- [Remote Tracking Branches](https://git-scm.com/book/en/v2/Git-Branching-Remote-Branches)
- [Editing Hunks Effectively](https://stackoverflow.com/questions/6276752/can-i-split-an-already-split-hunk-with-git/37769129#37769129) -- For those moments when splitting a hunk doesn't work (rare!)

### What's Next?

After you have completed this course, you are probably wondering where to go from here:

- [GitHub's On Demand Training](https://services.github.com/on-demand/)
- [Recommended Path for Learning More](https://services.github.com/on-demand/path/)
- [A Curated List of our Favorite Resources](https://services.github.com/classnotes/)
