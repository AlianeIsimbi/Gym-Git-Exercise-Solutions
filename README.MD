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