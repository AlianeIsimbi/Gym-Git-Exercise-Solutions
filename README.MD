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
### Exercise 2
```
brian@AlianeI23 MINGW64 ~/git-exercises (ft/bundle-2)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git pull
Already up to date.

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git checkout -b "ft/service-redesign"
Switched to a new branch 'ft/service-redesign'

brian@AlianeI23 MINGW64 ~/git-exercises (ft/service-redesign)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git pull
Already up to date.

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 902 bytes | 180.00 KiB/s, done.
From https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions
   4c56624..c57761b  main       -> origin/main
Updating 4c56624..c57761b
Fast-forward
 README.MD    | 61 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 about.html   | 11 +++++++++++
 home.html    | 11 +++++++++++
 service.html | 11 +++++++++++
 4 files changed, 94 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 service.html

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git switch ft/service-redesign 
Switched to branch 'ft/service-redesign'

brian@AlianeI23 MINGW64 ~/git-exercises (ft/service-redesign)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git switch dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.

brian@AlianeI23 MINGW64 ~/git-exercises (dev)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git checkout -b ft/service-redesign
fatal: a branch named 'ft/service-redesign' already exists

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git chechout -D ft/service-redesign
git: 'chechout' is not a git command. See 'git --help'.

The most similar command is
        checkout

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git checkout -D ft/service-redesign 
error: unknown switch `D'
usage: git checkout [<options>] <branch>
   or: git checkout [<options>] [<branch>] -- <file>...

    -b <branch>           create and checkout a new branch
    -B <branch>           create/reset and checkout a branch
    -l                    create reflog for new branch
    --[no-]guess          second guess 'git checkout <no-such-branch>' (default)
    --[no-]overlay        use overlay mode (default)
    -q, --[no-]quiet      suppress progress reporting
    --[no-]recurse-submodules[=<checkout>]
                          control recursive updating of submodules
    --[no-]progress       force progress reporting
    -m, --[no-]merge      perform a 3-way merge with the new branch
    --[no-]conflict <style>
                          conflict style (merge, diff3, or zdiff3)
    -d, --[no-]detach     detach HEAD at named commit
    -t, --[no-]track[=(direct|inherit)]
                          set branch tracking configuration
    -f, --[no-]force      force checkout (throw away local modifications)
    --[no-]orphan <new-branch>
                          new unborn branch
    --[no-]overwrite-ignore
                          update ignored files (default)
    --[no-]ignore-other-worktrees
                          do not check if another worktree is holding the given ref
    -2, --ours            checkout our version for unmerged files
    -3, --theirs          checkout their version for unmerged files
    -p, --[no-]patch      select hunks interactively
    --[no-]ignore-skip-worktree-bits
                          do not limit pathspecs to sparse entries only
    --[no-]pathspec-from-file <file>
                          read pathspec from file
    --[no-]pathspec-file-nul
                          with --pathspec-from-file, pathspec elements are separated with NUL character


brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git checkout -b ft/service-redesign
fatal: a branch named 'ft/service-redesign' already exists

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git branch -D ft/service-redesign 
Deleted branch ft/service-redesign (was 4c56624).

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

brian@AlianeI23 MINGW64 ~/git-exercises (ft/service-redesign)
$ git add --all

brian@AlianeI23 MINGW64 ~/git-exercises (ft/service-redesign)
$ git commit -m "Updated the service page"
[ft/service-redesign 22915a5] Updated the service page
 1 file changed, 8 insertions(+), 1 deletion(-)

brian@AlianeI23 MINGW64 ~/git-exercises (ft/service-redesign)
$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


brian@AlianeI23 MINGW64 ~/git-exercises (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 478 bytes | 478.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
brian@AlianeI23 MINGW64 ~/git-exercises (ft/service-redesign)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git add .

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git commit -m "Created a list of the old services"
[main 6fc9610] Created a list of the old services
 1 file changed, 8 insertions(+), 1 deletion(-)

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 484 bytes | 161.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions.git
   c57761b..6fc9610  main -> main

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git branch ft/service-redesign 
fatal: a branch named 'ft/service-redesign' already exists

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git switch ft/service-redesign 
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

brian@AlianeI23 MINGW64 ~/git-exercises (ft/service-redesign)
$ git merge main
Auto-merging service.html
CONFLICT (content): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.

brian@AlianeI23 MINGW64 ~/git-exercises (ft/service-redesign|MERGING)
$
 *  History restored 


brian@AlianeI23 MINGW64 ~/git-exercises (ft/service-redesign|MERGING)
$ git add .

brian@AlianeI23 MINGW64 ~/git-exercises (ft/service-redesign|MERGING)
$ git commit -m "Merging"
[ft/service-redesign bf4fe27] Merging

brian@AlianeI23 MINGW64 ~/git-exercises (ft/service-redesign)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 374 bytes | 374.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions.git
   b1b6c74..bf4fe27  ft/service-redesign -> ft/service-redesign

```