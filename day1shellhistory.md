cd Desktop
ls
mkdir classrepos
cd classrepos
ls
ls -al
cd ..
cd classrepos
atom .
git clone https://github.com/githubschool/ideal-train.git
git --version
git config --list
ls
cd ideal-train
git config --global user.name "Eric Hollenberry"
git config --global --list
git config --global user.email "hollenberry@github.com"
git config --global --list
git branch
git branch --all
cd ..
cd ideal-train
git checkout githubteacher-sandiego 
git remote -v
git branch
atom .
git status
git add githubteacher-sandiego.md
git status
git add githubteacher-sandiego.md
git status
git commit --message "Create githubteacher-sd file and add stubs"
git status
git push
git status
git add githubteacher-sandiego.md
git status
git commit -m "Add recs to San Diego file"
git push
git status
git pull
git checkout master
git pull
git status
git branch
git branch --merged
git branch -d githubteacher-sandiego 
git branch --all
git pull --prune
git config --global fetch.prune true
git branch --all
git config --global --unset fetch.prune
git config --global --list
git log
git log --oneline
git log --oneline --graph
gitk
git log --oneline --graph --decorate
git log --oneline --graph --decorate --all
git lol
git config --global alias.lol "log --oneline --graph --decorate --all"
git config --global alias.LOL "log"
git LOL
git config --global --list
git config --global alias.LOL "log"
git config --global alias.lol "log --oneline --graph --decorate --all"
clear
git s
git config --global alias.s "status"
git config --global --list
git checkout -b newbranch
echo newfile.md
touch newfile.md
git status
git add .
git commit -m "New
git commit -m "New"
git pull
git lol
touch newerfile.md
git status
git add .
git stash
git status
git checkout -b newestplace
git status
git stash pop
git stash list
git stash
git stash list
git stash --help
touch morework.md
git status
git stash
git add .
git commit -m "Add more work"
echo "text" >> morework.md
git status
git stash
git stash --list
git stash list
echo "newer text" >> morework.md
git checkout master
