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