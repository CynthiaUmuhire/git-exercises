# git-exercises

### Bundle 1

## Exercise 1

```bash
umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git init
Reinitialized existing Git repository in D:/git-exercises/.git/

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ touch file.html

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ echo "I am cute" > test.html

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ cat > new.html
hiiiii
umuhi@IKYK MINGW64 /d/git-exercises (main)
$ mv new.html textfile.txt

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ rm test.html

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git add .

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git commit -m 'making changes with my files (deletung, adding and renaming)'
[main bdc2967] making changes with my files (deletung, adding and renaming)
 3 files changed, 9 insertions(+), 1 deletion(-)
 create mode 100644 file.html
 create mode 100644 textfile.txt

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 433 bytes | 108.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/CynthiaUmuhire/git-exercises.git
   c8c9b11..bdc2967  main -> main

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git checkout dev
error: pathspec 'dev' did not match any file(s) known to git

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git branch dev

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git checkout dev
Switched to branch 'dev'

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git branch test

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git checkout test
Switched to branch 'test'

umuhi@IKYK MINGW64 /d/git-exercises (test)
$ git branch dev
fatal: a branch named 'dev' already exists

umuhi@IKYK MINGW64 /d/git-exercises (test)
$ git checkout dev
Switched to branch 'dev'

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git add .

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git commit -m 'creating new branches dev and test'
On branch dev
nothing to commit, working tree clean

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

$ git push --set-upstream origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/CynthiaUmuhire/git-exercises/pull/new/dev
remote:
To https://github.com/CynthiaUmuhire/git-exercises.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git branch -d test
Deleted branch test (was bdc2967).
```

# Bundle 2 
## Exercise 1

### Execise 2
```bash

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean
umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ touch home.html

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git stash list

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git add home.html

umuhi@IKYK MINGW64 /d/git-exercises (dev)
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md


umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git stash
$ git stash list
stash@{0}: WIP on dev: bdc2967 making changes with my files (deletung, adding and renaming)   

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ touch about.html

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git add about.html

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git stash
Saved working directory and index state WIP on dev: bdc2967 making changes with my files (deletung, adding and renaming)

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git stash list
stash@{0}: WIP on dev: bdc2967 making changes with my files (deletung, adding and renaming)   
stash@{1}: WIP on dev: bdc2967 making changes with my files (deletung, adding and renaming)   

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ touch team.html

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git addd team.html
git: 'addd' is not a git command. See 'git --help'.

The most similar command is
        add

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git add team.html

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git stash 
Saved working directory and index state WIP on dev: bdc2967 making changes with my files (deletung, adding and renaming)

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git stash list
stash@{0}: WIP on dev: bdc2967 making changes with my files (deletung, adding and renaming)
stash@{1}: WIP on dev: bdc2967 making changes with my files (deletung, adding and renaming)   
stash@{2}: WIP on dev: bdc2967 making changes with my files (deletung, adding and renaming)   

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git pop stash@{2}
git: 'pop' is not a git command. See 'git --help'.

The most similar command is
        log

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git stash pop stash@{2}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Dropped stash@{2} (665fdb5e6cb51a34d0026d6e20cb86e9eb6707ce)

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git stash list
stash@{0}: WIP on dev: bdc2967 making changes with my files (deletung, adding and renaming)
stash@{1}: WIP on dev: bdc2967 making changes with my files (deletung, adding and renaming)   

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Dropped stash@{1} (81f44eb32bf2d2ecfc490a63193f381a474e040f)

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git commit -m 'stashing and unstashing mythe home and about pages'
[dev d61b0ae] stashing and unstashing mythe home and about pages
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git push 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 647 bytes | 107.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/CynthiaUmuhire/git-exercises.git
   bdc2967..d61b0ae  dev -> dev

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git stash list
stash@{0}: WIP on dev: bdc2967 making changes with my files (deletung, adding and renaming)

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git stah pop stash@{0}
git: 'stah' is not a git command. See 'git --help'.

The most similar command is
        stash

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Dropped stash@{0} (c1e4c00d9933cf472e37061bc4ee90fd82f45ee3)

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$ git reset --hard
HEAD is now at d61b0ae stashing and unstashing mythe home and about pages

umuhi@IKYK MINGW64 /d/git-exercises (dev)
$
```
### Exercise 2 
```bash
umuhi@IKYK MINGW64 /d/git-exercises (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 3 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git pull
Updating bdc2967..35ae1ff
Fast-forward
 README.md     | 282 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 about.html    |  11 +++
 home.html     |  11 +++
 services.html |  12 +++
 4 files changed, 314 insertions(+), 2 deletions(-)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git branch ft/service-redesign

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

umuhi@IKYK MINGW64 /d/git-exercises (ft/service-redesign)
$ git commit -m 'new changes to the service page'
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

umuhi@IKYK MINGW64 /d/git-exercises (ft/service-redesign)
$ git add services.html

umuhi@IKYK MINGW64 /d/git-exercises (ft/service-redesign)
$ git commit -m 'new changes to the service page'
[ft/service-redesign 57bab66] new changes to the service page
 1 file changed, 5 insertions(+), 1 deletion(-)

umuhi@IKYK MINGW64 /d/git-exercises (ft/service-redesign)
$ git push

umuhi@IKYK MINGW64 /d/git-exercises (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 376 bytes | 125.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/CynthiaUmuhire/git-exercises/pull/new/ft/service-redesign     
remote:
To https://github.com/CynthiaUmuhire/git-exercises.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

umuhi@IKYK MINGW64 /d/git-exercises (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git add services.html

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git commit -m ' the changes on the services page in the main branch'
[main 3a03f1c]  the changes on the services page in the main branch
 1 file changed, 1 insertion(+), 1 deletion(-)

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 377 bytes | 125.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/CynthiaUmuhire/git-exercises.git
   35ae1ff..3a03f1c  main -> main

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git checkout  ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

umuhi@IKYK MINGW64 /d/git-exercises (ft/service-redesign)
$ git diff ft/services-redesign main
fatal: ambiguous argument 'ft/services-redesign': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

umuhi@IKYK MINGW64 /d/git-exercises (ft/service-redesign)
$ git diff ft/service-redesign main
diff --git a/services.html b/services.html
index 2c5d68b..8bca958 100644
--- a/services.html
+++ b/services.html
@@ -1,16 +1,12 @@
 <!DOCTYPE html>
 <html lang="en">
-
 <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>SERVICES</title>
 </head>
-
 <body>
     <h1> our servicessss!!!</h1>
-    <h2>Come and enjoy them yourself</h2>
-
+    <h2> come and enjoy them yourself</h2>
 </body>
-
 </html>
\ No newline at end of file

umuhi@IKYK MINGW64 /d/git-exercises (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git merge ft/service-redesign
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html    
Automatic merge failed; fix conflicts and then commit the result.

umuhi@IKYK MINGW64 /d/git-exercises (main|MERGING)     
services.html: needs merge

umuhi@IKYK MINGW64 /d/git-exercises (main|MERGING)
$ git reset
Unstaged changes after reset:
M       services.html

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git checkout  ft/service-redesign
error: Your local changes to the following files would be overwritten by checkout:
        services.html
Please commit your changes or stash them before you switch branches.
Aborting

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git merge ft/service-redesign
error: Your local changes to the following files would be overwritten by merge:
        services.html
Please commit your changes or stash them before you merge.
Aborting
Merge with strategy ort failed.

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git add services.html

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git commit -m 'accepting the current changes form the ft/service-redesign branch'
[main c1eb536] accepting the current changes form the ft/service-redesign branch
 1 file changed, 5 insertions(+), 1 deletion(-)

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git merge ft/ft/service-redesign
merge: ft/ft/service-redesign - not something we can merge

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git merge ft/service-redesign
Merge made by the 'ort' strategy.

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git add .

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git commit -m 'the merge between the ft/service-redesign branch and the main branch aboot th
e changes made on the services.html file. '
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git push
Enumerating objects: 2, done.
Counting objects: 100% (2/2), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 387 bytes | 193.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/CynthiaUmuhire/git-exercises.git
   3a03f1c..9834769  main -> main

umuhi@IKYK MINGW64 /d/git-exercises (main)
$
```
## Bundle 3
### Exercise 1
```bash
umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git branch ft/team-page

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
M       README.md

umuhi@IKYK MINGW64 /d/git-exercises (ft/team-page)
$ touch team.html

umuhi@IKYK MINGW64 /d/git-exercises (ft/team-page)
$ git add team.html 

umuhi@IKYK MINGW64 /d/git-exercises (ft/team-page)
$ git commit -m 'the new team page'
[ft/team-page c119783] the new team page
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

umuhi@IKYK MINGW64 /d/git-exercises (ft/team-page)
$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


umuhi@IKYK MINGW64 /d/git-exercises (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 459 bytes | 229.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/CynthiaUmuhire/git-exercises/pull/new/ft/team-page
remote:
To https://github.com/CynthiaUmuhire/git-exercises.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

umuhi@IKYK MINGW64 /d/git-exercises (ft/team-page)
$ git checkout main 
Switched to branch 'main'
M       README.md
Your branch is up to date with 'origin/main'.

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git branch ft/contact-page

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
M       README.md
Your branch is up to date with 'origin/ft/team-page'.

umuhi@IKYK MINGW64 /d/git-exercises (ft/team-page)
$ git log 
commit c1197839f49923d4386f5ec72b07986c944be8d1 (HEAD -> ft/team-page, origin/ft/team-page)   
Author: Cynthia <109437062+CynthiaUmuhire@users.noreply.github.com>
Date:   Wed Jul 26 11:13:06 2023 +0200

    the new team page

commit 6a0b6247c040d43f5208b52c811d8586fcfeec2f (origin/main, origin/HEAD, main, ft/contact-page)
Author: Cynthia <109437062+CynthiaUmuhire@users.noreply.github.com>
Date:   Wed Jul 26 11:05:57 2023 +0200

    The readme file for my codes

commit 9834769648f33b8060d0fe152a3104213a0e8f6f
.github.com>
Date:   Wed Jul 26 10:59:07 2023 +0200

umuhi@IKYK MINGW64 /d/git-exercises (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'
M       README.md

umuhi@IKYK MINGW64 /d/git-exercises (ft/contact-page)
$ git cherry-pick c1197839f49923d4386f5ec72b07986c944be8d1
[ft/contact-page e5e4ab2] the new team page
 Date: Wed Jul 26 11:13:06 2023 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

umuhi@IKYK MINGW64 /d/git-exercises (ft/contact-page)
$ git add contact.html

umuhi@IKYK MINGW64 /d/git-exercises (ft/contact-page)
$ git commit -m 'new changes to the contact page'
[ft/contact-page b7a3fd1] new changes to the contact page
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html

umuhi@IKYK MINGW64 /d/git-exercises (ft/contact-page)
$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


umuhi@IKYK MINGW64 /d/git-exercises (ft/contact-page)
$  git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 767 bytes | 383.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/CynthiaUmuhire/git-exercises/pull/new/ft/contact-page
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

umuhi@IKYK MINGW64 /d/git-exercises (ft/contact-page)
$ git branch ft/faq-page

umuhi@IKYK MINGW64 /d/git-exercises (ft/contact-page)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'
M       README.md

umuhi@IKYK MINGW64 /d/git-exercises (ft/faq-page)
$ touch faq.html

umuhi@IKYK MINGW64 /d/git-exercises (ft/faq-page)
$ git add .

umuhi@IKYK MINGW64 /d/git-exercises (ft/faq-page)
$ git commit -m 'the faq page'
[ft/faq-page 2bac9bf] the faq page
 2 files changed, 14 insertions(+), 1 deletion(-)
 create mode 100644 faq.html

umuhi@IKYK MINGW64 /d/git-exercises (ft/faq-page)
$ git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


umuhi@IKYK MINGW64 /d/git-exercises (ft/faq-page)
$ ^C

Revert "the new team page"
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 544 bytes | 108.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/CynthiaUmuhire/git-exercises/pull/new/ft/faq-page
remote:
To https://github.com/CynthiaUmuhire/git-exercises.git
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
umuhi@IKYK MINGW64 /d/git-exercises (ft/faq-page)
$ git revert  56a37c14b0c3d0393e2421b6620b65dac5858186
hint: Waiting for your editor to close the file... Debugger listening on ws://127.0.0.1:56756/88edd04d-0676-4e7a-b0dd-e252c289f6fa     
For help, see: https://nodejs.org/en/docs/inspector
Debugger attached.
Waiting for the debugger to disconnect...    
[ft/faq-page 01229ca] Revert "the new team"
 1 file changed, 12 deletions(-)
 delete mode 100644 team.html
```
### Exercise 2 
```bash
umuhi@IKYK MINGW64 /d/git-exercises (ft/faq-page)
$ git branch ft/home-page-redesign

umuhi@IKYK MINGW64 /d/git-exercises (ft/faq-page)
$ git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 7 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git add home.html

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git commit -m 'adding an exclamation mark in the home.html page'
[main baab7a5] adding an exclamation mark in the home.html page
 1 file changed, 1 insertion(+), 1 deletion(-)

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git push
To https://github.com/CynthiaUmuhire/git-exercises.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/CynthiaUmuhire/git-exercises.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git pull
error: Your local changes to the following files would be overwritten by merge:
        README.md
Please commit your changes or stash them before you merge.
Aborting
$ git add .

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git commit -m 'commiting my changes  before pulling in the main branch'
[main 7270613] commiting my changes  before pulling in the main branch
 1 file changed, 1 insertion(+), 1 deletion(-)

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git pull
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

umuhi@IKYK MINGW64 /d/git-exercises (main|MERGING)
$ git pull
Already up to date.

umuhi@IKYK MINGW64 /d/git-exercises (main)
$ git push
lved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".       
Could not apply 6cf7a72... The Readme file for the codes

umuhi@IKYK MINGW64 /d/git-exercises (ft/home-page-redesign|REBASE 2/2)
$ git rebase main
Current branch ft/home-page-redesign is up to date.

umuhi@IKYK MINGW64 /d/git-exercises (ft/home-page-redesign)
$ git add .

umuhi@IKYK MINGW64 /d/git-exercises (ft/home-page-redesign)
$ git commit -m 'the chaanges to the home page'
[ft/home-page-redesign 43643bb] the chaanges to the home page
 1 file changed, 1 insertion(+)

umuhi@IKYK MINGW64 /d/git-exercises (ft/home-page-redesign)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/CynthiaUmuhire/git-exercises.git
   2de060e..43643bb  ft/home-page-redesign -> ft/home-page-redesign

```