# Git exercise
## Bundle 1
### Exercise 1
```
brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.MD

no changes added to commit (use "git add" and/or "git commit -a")
brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git checkout -b dev
Switched to a new branch 'dev'

brian@AlianeI23 MINGW64 ~/git-exercises (dev)
$ git checkout -b test
Switched to a new branch 'test'

brian@AlianeI23 MINGW64 ~/git-exercises (test)
$ git switch dev
Switched to branch 'dev'

brian@AlianeI23 MINGW64 ~/git-exercises (dev)
$ git branch -d test
Deleted branch test (was 4c56624).

```
### Exercise 2
```
brian@AlianeI23 MINGW64 ~/git-exercises (dev)   
$ git stash list
stash@{0}: WIP on dev: c3ff11c New changes
stash@{1}: WIP on dev: c3ff11c New changes      
stash@{2}: WIP on dev: c3ff11c New changes      

brian@AlianeI23 MINGW64 ~/git-exercises (dev)   
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.    

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (f70b7ed83245fa2afbab0a0d8b432d034f53d2a5)

brian@AlianeI23 MINGW64 ~/git-exercises (dev)   
$ git stash list
stash@{0}: WIP on dev: c3ff11c New changes
stash@{1}: WIP on dev: c3ff11c New changes      

brian@AlianeI23 MINGW64 ~/git-exercises (dev)   
$ git stash pop ^[[200~stash@{0}~
error: ?[200~stash@{0}~ is not a valid reference

brian@AlianeI23 MINGW64 ~/git-exercises (dev)   
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.    

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   team.html

Dropped stash@{0} (e2cf9c4e646ec9b0827871826b61174d9170620e)

brian@AlianeI23 MINGW64 ~/git-exercises (dev)   
$ git stash list
stash@{0}: WIP on dev: c3ff11c New changes

brian@AlianeI23 MINGW64 ~/git-exercises (dev)   
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.    

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
        new file:   team.html

Dropped stash@{0} (5c4b3abbd30b2282ad457bf027ed48562d267f72)

brian@AlianeI23 MINGW64 ~/git-exercises (dev)   
$ git stash list

brian@AlianeI23 MINGW64 ~/git-exercises (dev)   
$
 *  History restored 


brian@AlianeI23 MINGW64 ~/git-exercises (dev)   
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.MD


brian@AlianeI23 MINGW64 ~/git-exercises (dev)   
$ git add --all
$ git stash team.html
fatal: subcommand wasn't specified; 'push' can't be assumed due to unexpected token 'team.html'

brian@AlianeI23 MINGW64 ~/git-exercises (dev)
$ git add team.html

brian@AlianeI23 MINGW64 ~/git-exercises (dev)
$ git stash
Saved working directory and index state WIP on dev: c3ff11c New changes

brian@AlianeI23 MINGW64 ~/git-exercises (dev)
$ git stash list
stash@{0}: WIP on dev: c3ff11c New changes
```