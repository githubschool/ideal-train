cd ..
git clone https://github.com/githubtraining/github-games-1.git
git branch readme-update
cd github-games-1
git branch readme-update
git branch
git checkout readme-update
atom .
git status
git add README.md
git commit -m "Adjust URL to my gh page"
git push
git push --set-upstream origin readme-update
git branch -v
git checkout master
git branch -d readme-update 
git pull --prune
git branch --all
git branch
git lol
git config --global alias.lol "log --oneline --graph --decorate --all"
git lol
git checkout stats-update
git merge gh-pages
git merge master
git status
git add inde.html
git status
git commit
git checkout master
git merge stats-update
git push
git lol
git bisect start
git status
git bisect bad HEAD
git bisect good ea054de
ls
git bisect bad
ls
git bisect good
ls
git bisect good
git bisect reset
git blame
git blame f99c7219108337b35abac4e33e0edcb5fb470bdf
ls
git bisect start HEAD ea05
git bisect run ls index.html
git bisect reset
git show f99c
git show d285
git revert f99c
git push
git remote 
git remote -v
git remote add upstream https://github.com/hollenberry/github-games-1.git
git remote
git remote -v
git branch --all
git pull
git fetch upstream
git branch --all
git checkout shape-colors
git checkout -b shape-colors
git checkout master
git branch -d shape-colors
git checkout -b shape-colors origin/shape-colors
git branch --help
git branch
git branch -v
git branch -vv
git s
git add .
git s
git commit -m "Change colors to green"
git merge upstream/shape-colors
git status
git commit
git push
git pull
git pull shape-colors
git fetch origin
git pull origin/shape-colors
git pull origin shape-colors
git checkout master
git merge shape-colors
git pull
atom .
git status
git add .
git commit 
git push
git checkout -b change-speed
mkdir images
git status
git mv texture.jpg images/texture.jpg
git status
git add -p
atom .
git status
git commit -m "Moved the texture file into dir"
git status
git add -p
git status
git commit -m "Change start speed of block to .3"
git status
git checkout -- .
git status
git add -p
git commit -m "Resolve merge conflict"
git status
git add -p
git status
git add -p
git status
git fetch
git fetch origin
git lol
git diff
git status
git diff --staged
git diff HEAD
git diff master
git lol
git diff HEAD e35bdeb
git lol
git diff HEAD ebc97e4
cd ..
git init practice-repo
ls
cd prac
cd practice-repo
ls
ls -al
tree .git
cat .git/HEAD
cat .git/refs/heads/master
touch README.md
git status
tree .git
git add .
tree .git
git commit -m "Add readme"
tree .git
git lol
cat .git/refs/heads/master
for d in {1..6}; do touch file$d.md; git add file$d.md; git commit -m "adding file $d"; done
git lol
git reset --mixed HEAD~
git lol
git status
git add .
git commit -m "Add file 6"
git reset --soft HEAD~2
git lol
git status
git add .
git commit -m "Add 5 file and 6"
git lol
git reset --hard 50b
git reset --hard 50b6
git lol
git reflog 
git cherry-pick a2a05f1 7a7c5e0 162a2da
git lol
cd ..
mkdir practice-repo2
cd practice-repo
cd ..
cd practice-repo2
git init
touch readme.md
git add .
git commit -m "Add readme"
git lol
cd ..
ll
git lol
cd ..
cd classrepos
cd ideal-train
git lol
git push
git push -u origin newestplace
git branch
git checkout newbranch
git add .
git commit -m "stay"
git checkout newbranch
git status
git lol
git push -u origin newbranch
git pull
git checkout sureshk-SFO
git rebase master
git push
git checkout master
git pull
git push
git pull
git lol
git status
git pull
git pull -f
git reset --hard 566
git reset --hard 566b
git pull
tree .git
git pull
git lol
git branch -d sureshk-SFO 
git pull
git checkout newbranch2
git rebase master
git checkout master
git checkout newbranch2
git rebase newbranch2 master
git status
git lol
git push
git branch
git branch -d newbranch
git branch -d newbranch2 
git checkout practice-repo
cd ..
cd practice-repo
git remote -v
git remote add origin https://github.com/githubteacher/practice-repo2.git
: 1500583370:0;git push -u origin master
