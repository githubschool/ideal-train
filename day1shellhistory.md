: 1500476282:0;cd ..
: 1500476285:0;cd training-utils
: 1500476290:0;ls
: 1500476295:0;historytailzsh 10 10 
: 1500483378:0;ls
: 1500483411:0;cd Desktop
: 1500483425:0;ls
: 1500483444:0;mkdir classrepos
: 1500483479:0;cd classrepos
: 1500483528:0;ls
: 1500483533:0;ls -al
: 1500483559:0;cd ..
: 1500483562:0;cd classrepos
: 1500483570:0;atom .
: 1500483732:0;git clone https://github.com/githubschool/ideal-train.git
: 1500483869:0;git --version
: 1500483930:0;git config --list
: 1500483998:0;ls
: 1500484001:0;cd ideal-train
: 1500484089:0;git config --global user.name "Eric Hollenberry"
: 1500484107:0;git config --global --list
: 1500484129:0;git config --global user.email "hollenberry@github.com"
: 1500484249:0;git config --global --list
: 1500484365:0;git branch
: 1500484383:0;git branch --all
: 1500484412:0;cd ..
: 1500484416:0;cd ideal-train
: 1500484498:0;git checkout githubteacher-sandiego 
: 1500484893:0;git remote -v
: 1500484943:0;git branch
: 1500485074:0;atom .
: 1500485378:0;git status
: 1500485438:0;git add githubteacher-sandiego.md
: 1500485447:0;git status
: 1500485691:0;git add githubteacher-sandiego.md
: 1500485693:0;git status
: 1500485778:0;git commit --message "Create githubteacher-sd file and add stubs"
: 1500485880:0;git status
: 1500485895:0;git push
: 1500491474:0;git status
: 1500491499:0;git add githubteacher-sandiego.md
: 1500491504:0;git status
: 1500491531:0;git commit -m "Add recs to San Diego file"
: 1500491550:0;git push
: 1500493833:0;git status
: 1500493852:0;git pull
: 1500493883:0;git checkout master
: 1500493903:0;git pull
: 1500493914:0;git status
: 1500493935:0;git branch
: 1500494039:0;git branch --merged
: 1500494059:0;git branch -d githubteacher-sandiego 
: 1500494095:0;git branch --all
: 1500494117:0;git pull --prune
: 1500494157:0;git config --global fetch.prune true
: 1500494236:0;git branch --all
: 1500494489:0;git config --global --unset fetch.prune
: 1500494493:0;git config --global --list
: 1500495165:0;git log
: 1500495213:0;git log --oneline
: 1500495239:0;git log --oneline --graph
: 1500495260:0;gitk
: 1500495356:0;git log --oneline --graph --decorate
: 1500495363:0;git log --oneline --graph --decorate --all
: 1500495387:0;git lol
: 1500495462:0;git config --global alias.lol "log --oneline --graph --decorate --all"
: 1500495471:0;git config --global alias.LOL "log"
: 1500495473:0;git LOL
: 1500495480:0;git config --global --list
: 1500495505:0;git config --global alias.LOL "log"
: 1500495507:0;git config --global alias.lol "log --oneline --graph --decorate --all"
: 1500495537:0;clear
: 1500495558:0;git s
: 1500495648:0;git config --global alias.s "status"
: 1500495672:0;git config --global --list
: 1500496253:0;git checkout -b newbranch
: 1500496259:0;echo newfile.md
: 1500496262:0;touch newfile.md
: 1500496264:0;git status
: 1500496266:0;git add .
: 1500496281:0;git commit -m "New
: 1500496284:0;git commit -m "New"
: 1500496473:0;git pull
: 1500496535:0;git lol
: 1500497397:0;touch newerfile.md
: 1500497400:0;git status
: 1500497401:0;git add .
: 1500497418:0;git stash
: 1500497437:0;git status
: 1500497445:0;git checkout -b newestplace
: 1500497449:0;git status
: 1500497455:0;git stash pop
: 1500497653:0;git stash list
: 1500497657:0;git stash
: 1500497659:0;git stash list
: 1500497666:0;git stash --help
: 1500497721:0;touch morework.md
: 1500497726:0;git status
: 1500497727:0;git stash
: 1500497743:0;git add .
: 1500497757:0;git commit -m "Add more work"
: 1500497777:0;echo "text" >> morework.md
: 1500497781:0;git status
: 1500497784:0;git stash
: 1500497790:0;git stash --list
: 1500497793:0;git stash list
: 1500498157:0;echo "newer text" >> morework.md
: 1500498160:0;git checkout master
