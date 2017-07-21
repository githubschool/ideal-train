: 1500565531:0;cd ..
: 1500565539:0;git clone https://github.com/githubtraining/github-games-1.git
: 1500565734:0;git branch readme-update
: 1500565738:0;cd github-games-1
: 1500565745:0;git branch readme-update
: 1500565768:0;git branch
: 1500565827:0;git checkout readme-update
: 1500565839:0;atom .
: 1500565918:0;git status
: 1500565938:0;git add README.md
: 1500565977:0;git commit -m "Adjust URL to my gh page"
: 1500566017:0;git push
: 1500566060:0;git push --set-upstream origin readme-update
: 1500566109:0;git branch -v
: 1500566595:0;git checkout master
: 1500566616:0;git branch -d readme-update 
: 1500566654:0;git pull --prune
: 1500566686:0;git branch --all
: 1500566745:0;git branch
: 1500567519:0;git lol
: 1500567554:0;git config --global alias.lol "log --oneline --graph --decorate --all"
: 1500567588:0;git lol
: 1500568014:0;git checkout stats-update
: 1500568040:0;git merge gh-pages
: 1500568045:0;git merge master
: 1500568291:0;git status
: 1500568325:0;git add inde.html
: 1500568334:0;git status
: 1500568368:0;git commit
: 1500568781:0;git checkout master
: 1500568786:0;git merge stats-update
: 1500568802:0;git push
: 1500569386:0;git lol
: 1500569412:0;git bisect start
: 1500569423:0;git status
: 1500569467:0;git bisect bad HEAD
: 1500569478:0;git bisect good ea054de
: 1500569659:0;ls
: 1500569675:0;git bisect bad
: 1500569677:0;ls
: 1500569685:0;git bisect good
: 1500569686:0;ls
: 1500569690:0;git bisect good
: 1500569830:0;git bisect reset
: 1500570048:0;git blame
: 1500570064:0;git blame f99c7219108337b35abac4e33e0edcb5fb470bdf
: 1500570352:0;ls
: 1500570419:0;git bisect start HEAD ea05
: 1500570479:0;git bisect run ls index.html
: 1500570522:0;git bisect reset
: 1500570911:0;git show f99c
: 1500570956:0;git show d285
: 1500571013:0;git revert f99c
: 1500571208:0;git push
: 1500571968:0;git remote 
: 1500571975:0;git remote -v
: 1500572024:0;git remote add upstream https://github.com/hollenberry/github-games-1.git
: 1500572035:0;git remote
: 1500572039:0;git remote -v
: 1500572120:0;git branch --all
: 1500572130:0;git pull
: 1500572253:0;git fetch upstream
: 1500572299:0;git branch --all
: 1500572323:0;git checkout shape-colors
: 1500572351:0;git checkout -b shape-colors
: 1500572388:0;git checkout master
: 1500572391:0;git branch -d shape-colors
: 1500572412:0;git checkout -b shape-colors origin/shape-colors
: 1500572532:0;git branch --help
: 1500572546:0;git branch
: 1500572556:0;git branch -v
: 1500572598:0;git branch -vv
: 1500572729:0;git s
: 1500572769:0;git add .
: 1500572771:0;git s
: 1500572782:0;git commit -m "Change colors to green"
: 1500572980:0;git merge upstream/shape-colors
: 1500573356:0;git status
: 1500573366:0;git commit
: 1500573408:0;git push
: 1500577713:0;git pull
: 1500577739:0;git pull shape-colors
: 1500577752:0;git fetch origin
: 1500577761:0;git pull origin/shape-colors
: 1500577782:0;git pull origin shape-colors
: 1500577873:0;git checkout master
: 1500577879:0;git merge shape-colors
: 1500577895:0;git pull
: 1500577943:0;atom .
: 1500578062:0;git status
: 1500578064:0;git add .
: 1500578068:0;git commit 
: 1500578125:0;git push
: 1500578198:0;git checkout -b change-speed
: 1500578337:0;mkdir images
: 1500578357:0;git status
: 1500578387:0;git mv texture.jpg images/texture.jpg
: 1500578389:0;git status
: 1500578445:0;git add -p
: 1500578560:0;atom .
: 1500578572:0;git status
: 1500578601:0;git commit -m "Moved the texture file into dir"
: 1500578607:0;git status
: 1500578625:0;git add -p
: 1500578658:0;git status
: 1500578671:0;git commit -m "Change start speed of block to .3"
: 1500578675:0;git status
: 1500578688:0;git checkout -- .
: 1500578700:0;git status
: 1500578702:0;git add -p
: 1500578739:0;git commit -m "Resolve merge conflict"
: 1500578763:0;git status
: 1500578765:0;git add -p
: 1500578800:0;git status
: 1500578802:0;git add -p
: 1500579002:0;git status
: 1500579141:0;git fetch
: 1500579144:0;git fetch origin
: 1500579147:0;git lol
: 1500579225:0;git diff
: 1500579235:0;git status
: 1500579239:0;git diff --staged
: 1500579278:0;git diff HEAD
: 1500579290:0;git diff master
: 1500579304:0;git lol
: 1500579313:0;git diff HEAD e35bdeb
: 1500579369:0;git lol
: 1500579390:0;git diff HEAD ebc97e4
: 1500580115:0;cd ..
: 1500580141:0;git init practice-repo
: 1500580152:0;ls
: 1500580157:0;cd prac
: 1500580159:0;cd practice-repo
: 1500580181:0;ls
: 1500580193:0;ls -al
: 1500580203:0;tree .git
: 1500580286:0;cat .git/HEAD
: 1500580368:0;cat .git/refs/heads/master
: 1500580434:0;touch README.md
: 1500580436:0;git status
: 1500580444:0;tree .git
: 1500580451:0;git add .
: 1500580468:0;tree .git
: 1500580489:0;git commit -m "Add readme"
: 1500580493:0;tree .git
: 1500580505:0;git lol
: 1500580557:0;cat .git/refs/heads/master
: 1500581338:0;for d in {1..6}; do touch file$d.md; git add file$d.md; git commit -m "adding file $d"; done
: 1500581341:0;git lol
: 1500581382:0;git reset --mixed HEAD~
: 1500581390:0;git lol
: 1500581396:0;git status
: 1500581408:0;git add .
: 1500581412:0;git commit -m "Add file 6"
: 1500581464:0;git reset --soft HEAD~2
: 1500581467:0;git lol
: 1500581471:0;git status
: 1500581516:0;git add .
: 1500581526:0;git commit -m "Add 5 file and 6"
: 1500581527:0;git lol
: 1500581695:0;git reset --hard 50b
: 1500581700:0;git reset --hard 50b6
: 1500581705:0;git lol
: 1500581734:0;git reflog 
: 1500581803:0;git cherry-pick a2a05f1 7a7c5e0 162a2da
: 1500581805:0;git lol
: 1500581931:0;cd ..
: 1500581938:0;mkdir practice-repo2
: 1500581940:0;cd practice-repo
: 1500581943:0;cd ..
: 1500581945:0;cd practice-repo2
: 1500581947:0;git init
: 1500581956:0;touch readme.md
: 1500581958:0;git add .
: 1500581962:0;git commit -m "Add readme"
: 1500581981:0;git lol
: 1500582071:0;cd ..
: 1500582310:0;ll
: 1500582312:0;git lol
: 1500582313:0;cd ..
: 1500582316:0;cd classrepos
: 1500582329:0;cd ideal-train
: 1500582347:0;git lol
: 1500582356:0;git push
: 1500582361:0;git push -u origin newestplace
: 1500582502:0;git branch
: 1500582513:0;git checkout newbranch
: 1500582520:0;git add .
: 1500582522:0;git commit -m "stay"
: 1500582525:0;git checkout newbranch
: 1500582527:0;git status
: 1500582528:0;git lol
: 1500582533:0;git push -u origin newbranch
: 1500582596:0;git pull
: 1500582608:0;git checkout sureshk-SFO
: 1500582621:0;git rebase master
: 1500582623:0;git push
: 1500582645:0;git checkout master
: 1500582648:0;git pull
: 1500582651:0;git push
: 1500582656:0;git pull
: 1500582666:0;git lol
: 1500582676:0;git status
: 1500582679:0;git pull
: 1500582681:0;git pull -f
: 1500582698:0;git reset --hard 566
: 1500582700:0;git reset --hard 566b
: 1500582703:0;git pull
: 1500582747:0;tree .git
: 1500582764:0;git pull
: 1500582773:0;git lol
: 1500582782:0;git branch -d sureshk-SFO 
: 1500582786:0;git pull
: 1500582853:0;git checkout newbranch2
: 1500582890:0;git rebase master
: 1500582893:0;git checkout master
: 1500582899:0;git checkout newbranch2
: 1500582904:0;git rebase newbranch2 master
: 1500582918:0;git status
: 1500582921:0;git lol
: 1500582927:0;git push
: 1500583075:0;git branch
: 1500583079:0;git branch -d newbranch
: 1500583086:0;git branch -d newbranch2 
: 1500583275:0;git checkout practice-repo
: 1500583278:0;cd ..
: 1500583281:0;cd practice-repo
: 1500583358:0;git remote -v
: 1500583366:0;git remote add origin https://github.com/githubteacher/practice-repo2.git
: 1500583370:0;git push -u origin master
