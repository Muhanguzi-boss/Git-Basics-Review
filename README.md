# Git Basics

## Bunde 1

### Exercise 1
```bash

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (main)
$ touch index.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (main)
$ touch basicgit.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (main)
$ git branch -m main master

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (master)
$ git add .

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (master)
$ git commit -m "First commit for the first exercise"
[master (root-commit) 29df94f] First commit for the first exercise
 2 files changed, 22 insertions(+)
 create mode 100644 basicgit.html
 create mode 100644 index.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (master)
$ git push -u origin master
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 505 bytes | 11.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Muhanguzi-boss/Git-Basics-Review.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (master)
$ git checkout -b dev
Switched to a new branch 'dev'

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git checkout -b test
Switched to a new branch 'test'

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (test)
$ git checkout dev
Switched to branch 'dev'

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git branch -d test
Deleted branch test (was 29df94f).

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git branch
* dev
  master

```

### Exercise 2
```bash
PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ touch home.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git add home.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git stash save "Added home.html file"
Saved working directory and index state On dev: Added home.html file

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ touch about.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git add about.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git stash save "Added about.html"
Saved working directory and index state On dev: Added about.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ touch team.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git add team.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git stash save "Added team.html file"
Saved working directory and index state On dev: Added team.html file

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

Dropped stash@{1} (d5e96fa788f4b1c0a7a75c89321c7b2f48730ce7)

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git stash pop stash@{2}
fatal: log for 'stash' only has 2 entries

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git stash list
stash@{0}: On dev: Added team.html file
stash@{1}: On dev: Added home.html file

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

Dropped stash@{1} (f1e750feb2be405d1b34248725728fc93dc9b900)

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git branch
* dev
  master

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (dev)
$ git checkout master
A       about.html
A       home.html
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (master)
$ git add .

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (master)
$ git commit -m "Restored and commited about.html and home.html files"
[master f0118ab] Restored and commited about.html and home.html files
 3 files changed, 89 insertions(+)
 create mode 100644 README.md
 create mode 100644 about.html
 create mode 100644 home.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (master)
$ git push
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 1.23 KiB | 38.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Muhanguzi-boss/Git-Basics-Review.git
   29df94f..f0118ab  master -> master

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (master)
$ git stash pop stash@{0}
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (6ef409d0c6506d0be912941ace792b0248af062d)

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (master)
$ git reset --hard HEAD
HEAD is now at f0118ab Restored and commited about.html and home.html files

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (master)
$

```

## Bundle 2
### Part 1
```bash
PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (master)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (ft/bundle-2)
$ touch services.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (ft/bundle-2)
$ git add services.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (ft/bundle-2)
$ git commit -m "Added services.html page"
[ft/bundle-2 7285ae7] Added services.html page
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 services.html

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 291 bytes | 58.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Muhanguzi-boss/Git-Basics-Review/pull/new/ft/bundle-2
remote:
To https://github.com/Muhanguzi-boss/Git-Basics-Review.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

PC@DESKTOP-083Q3R6 MINGW64 ~/Documents/Git-Basics-Review (ft/bundle-2)
$

```