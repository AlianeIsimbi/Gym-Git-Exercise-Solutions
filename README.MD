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
## Bundle 3
### Exercise 1
```
brian@AlianeI23 MINGW64 ~/git-exercises (ft/service-redesign)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

brian@AlianeI23 MINGW64 ~/git-exercises (ft/team-page)
$ git add team.html 

brian@AlianeI23 MINGW64 ~/git-exercises (ft/team-page)
$ git status
On branch ft/team-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html


brian@AlianeI23 MINGW64 ~/git-exercises (ft/team-page)
$ git commit -m "feat:Added a team branch"
[ft/team-page 98ae83d] feat:Added a team branch
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

brian@AlianeI23 MINGW64 ~/git-exercises (ft/team-page)
$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


brian@AlianeI23 MINGW64 ~/git-exercises (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 446 bytes | 223.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

brian@AlianeI23 MINGW64 ~/git-exercises (ft/team-page)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git checkout -b ft/contact page
fatal: 'page' is not a commit and a branch 'ft/contact' cannot be created from it

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git switch ft/team-page 
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

brian@AlianeI23 MINGW64 ~/git-exercises (ft/team-page)
$ git log
commit 98ae83d6708aa1c8cb8703f1e8fd91887b8947b9 (HEAD -> ft/team-page, origin/ft/team-page)
Author: AlianeIsimbi <isimbialiane@gmail.com>
Date:   Thu May 22 09:51:59 2025 +0200

    feat:Added a team branch

commit 6fc9610d2adbaa46c57cb1035f9cbcb6027bc4f4 (origin/main, main, ft/contact-page)
Author: AlianeIsimbi <isimbialiane@gmail.com>
Date:   Tue May 20 11:19:42 2025 +0200

    Created a list of the old services

commit c57761b57ca97085ec71c38eefc263c4d04a73c7
Merge: 4c56624 7d4ab8f
Author: Aliane ISIMBI <117778528+AlianeIsimbi@users.noreply.github.com>
Date:   Tue May 20 10:47:14 2025 +0200

:
commit 98ae83d6708aa1c8cb8703f1e8fd91887b8947b9 (HEAD -> ft/team-page, origin/ft/team-page)
Author: AlianeIsimbi <isimbialiane@gmail.com>
Date:   Thu May 22 09:51:59 2025 +0200

    feat:Added a team branch

commit 6fc9610d2adbaa46c57cb1035f9cbcb6027bc4f4 (origin/main, main, ft/contact-page)
Author: AlianeIsimbi <isimbialiane@gmail.com>
Date:   Tue May 20 11:19:42 2025 +0200

    Created a list of the old services

commit c57761b57ca97085ec71c38eefc263c4d04a73c7
Merge: 4c56624 7d4ab8f
Author: Aliane ISIMBI <117778528+AlianeIsimbi@users.noreply.github.com>
Date:   Tue May 20 10:47:14 2025 +0200


brian@AlianeI23 MINGW64 ~/git-exercises (ft/team-page)
$ git checkout ft/contact-page 
Switched to branch 'ft/contact-page'

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git cherry-pick 98ae83d6708aa1c8cb8703f1e8fd91887b8947b9
error: The following untracked working tree files would be overwritten by merge:
        team.html
Please move or remove them before you merge.
Aborting
fatal: cherry-pick failed

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git cherry-pick 98ae83d6708aa1c8cb8703f1e8fd91887b8947b9
error: The following untracked working tree files would be overwritten by merge:
        team.html
Please move or remove them before you merge.
Aborting
fatal: cherry-pick failed

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git switch ft/team-page
error: The following untracked working tree files would be overwritten by checkout:
        team.html
Please move or remove them before you switch branches.
Aborting

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git switch ft/team-page
error: The following untracked working tree files would be overwritten by checkout:
        team.html
Please move or remove them before you switch branches.
Aborting

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git checkout ft/team-page
error: The following untracked working tree files would be overwritten by checkout:
        team.html
Please move or remove them before you switch branches.
Aborting

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git add /
fatal: C:/Program Files/Git/: 'C:/Program Files/Git/' is outside repository at 'C:/Users/brian/git-exercises'

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git add .

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git status
On branch ft/contact-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html


brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git cherry-pick 98ae83d6708aa1c8cb8703f1e8fd91887b8947b9
error: your local changes would be overwritten by cherry-pick.
hint: commit your changes or stash them to proceed.
fatal: cherry-pick failed

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git commit -m 
error: switch `m' requires a value

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git commit -m 'changes on the contant page'
[ft/contact-page bfff0f6] changes on the contant page
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git cherry-pick 98ae83d6708aa1c8cb8703f1e8fd91887b8947b9
On branch ft/contact-page
You are currently cherry-picking commit 98ae83d.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

nothing to commit, working tree clean
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page|CHERRY-PICKING)
$  git commit --allow-empty
[ft/contact-page ecb05cf] feat:Added a team branch
 Date: Thu May 22 09:51:59 2025 +0200

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git add contact.html 

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git status
On branch ft/contact-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   contact.html


brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git commit -m "feat:Added the contact page"
[ft/contact-page 84bebb7] feat:Added the contact page
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git push --set-upstream origin ft/contact-page
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 12 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 829 bytes | 829.00 KiB/s, done.
Total 7 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

brian@AlianeI23 MINGW64 ~/git-exercises (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

brian@AlianeI23 MINGW64 ~/git-exercises (ft/faq-page)
$ git add faq.html 

brian@AlianeI23 MINGW64 ~/git-exercises (ft/faq-page)
$ git commit -m "added the FAQ page"
[ft/faq-page 6a7fd0c] added the FAQ page
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

brian@AlianeI23 MINGW64 ~/git-exercises (ft/faq-page)
$ git push --set-upstream origin ft/faq-page 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 441 bytes | 441.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

brian@AlianeI23 MINGW64 ~/git-exercises (ft/faq-page)
$ git revert 98ae83d6708aa1c8cb8703f1e8fd91887b8947b9
[ft/faq-page 14a2cae] Revert "feat:Added a team branch"
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html

brian@AlianeI23 MINGW64 ~/git-exercises (ft/faq-page)
$ git add .

brian@AlianeI23 MINGW64 ~/git-exercises (ft/faq-page)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 278 bytes | 278.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions.git
   6a7fd0c..14a2cae  ft/faq-page -> ft/faq-page
```
### Exercise 2
```

```
## Bundle 4
### Exercise 1
#### Switching to main
```
brian@AlianeI23 MINGW64 ~/git-exercises (ft/home-page-redesign)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
```
#### Adding another commit repo and commiting changes

```
brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git remote add Git-copy https://github.com/AlianeIsimbi/Git-copy.git

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git add .

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git commit -m "Added a new repo"
[main d620c75] Added a new repo
 1 file changed, 1 insertion(+), 1 deletion(-)
 ```
 #### Pushing changes to both repositories

```
brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git push Git-copy
Enumerating objects: 35, done.
Counting objects: 100% (35/35), done.
Delta compression using up to 12 threads
Compressing objects: 100% (33/33), done.
Writing objects: 100% (35/35), 6.58 KiB | 518.00 KiB/s, done.
Total 35 (delta 12), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (12/12), done.
To https://github.com/AlianeIsimbi/Git-copy.git
 * [new branch]      main -> main
```
### Exercise 2
#### Creating a new branch 'ft/footer' and pushing changes made
```
brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'

brian@AlianeI23 MINGW64 ~/git-exercises (ft/footer)
$ git add .

brian@AlianeI23 MINGW64 ~/git-exercises (ft/footer)
$ git commit "feat: Added the footer page"
error: pathspec 'feat: Added the footer page' did not match any file(s) known to git

brian@AlianeI23 MINGW64 ~/git-exercises (ft/footer)
$ git commit -m "feat: Added the footer page"
[ft/footer f8f92f4] feat: Added the footer page
 1 file changed, 11 insertions(+)
 create mode 100644 footer.html

brian@AlianeI23 MINGW64 ~/git-exercises (ft/footer)
$ git push
fatal: The current branch ft/footer has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/footer

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


brian@AlianeI23 MINGW64 ~/git-exercises (ft/footer)
$  git push --set-upstream origin ft/footer
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 806 bytes | 268.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions/pull/new/ft/footer
remote:
To https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.
```
#### Going back to main branch and creating a new branch 'ft/squashing'

```
brian@AlianeI23 MINGW64 ~/git-exercises (ft/footer)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

brian@AlianeI23 MINGW64 ~/git-exercises (main)
$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'
```
#### Merge squashing the changes in the 'ft/footer' branch, commiting and pushing changes

```
brian@AlianeI23 MINGW64 ~/git-exercises (ft/squashing)
$ git merge --squash ft/footer
Updating d620c75..f8f92f4
Fast-forward
Squash commit -- not updating HEAD
 footer.html | 11 +++++++++++
 1 file changed, 11 insertions(+)
 create mode 100644 footer.html

brian@AlianeI23 MINGW64 ~/git-exercises (ft/squashing)
$ git commit -m "footer changes squashing"
[ft/squashing 89d118c] footer changes squashing
 1 file changed, 11 insertions(+)
 create mode 100644 footer.html

brian@AlianeI23 MINGW64 ~/git-exercises (ft/squashing)
$ git push
fatal: The current branch ft/squashing has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/squashing

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


brian@AlianeI23 MINGW64 ~/git-exercises (ft/squashing)
$ git push --set-upstream origin ft/squashing
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 449 bytes | 149.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions/pull/new/ft/squashing
remote:
To https://github.com/AlianeIsimbi/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.
```