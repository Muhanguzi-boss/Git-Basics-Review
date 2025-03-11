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


```