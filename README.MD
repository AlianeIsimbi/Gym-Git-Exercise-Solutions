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
## Bundle 2
### Exercise 1
```
brian@AlianeI23 MINGW64 ~/git-exercises (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
brian@AlianeI23 MINGW64 ~/git-exercises (ft/bundle-2)
$ git add service.html 

brian@AlianeI23 MINGW64 ~/git-exercises (ft/bundle-2)
$ git commit -m "Created a services page"
[ft/bundle-2 25c98a4] Created a services page
 1 file changed, 11 insertions(+)
 create mode 100644 service.html

brian@AlianeI23 MINGW64 ~/git-exercises (ft/bundle-2)
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


brian@AlianeI23 MINGW64 ~/git-exercises (ft/bundle-2)
$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 461 bytes | 461.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.


```