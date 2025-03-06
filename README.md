# GIT EXERCISES
## Bundle 1
### Exercise 1
#### Task 1: Create a project folder & initialize git
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym$ mkdir Git\ Basics
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym$ cd Git\ Basics/
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
Initialized empty Git repository in /home/guhirwa/Documents/The Gym/Git Basics/.git/
```
#### Task 2: Make changes to the project (add files and contents) 
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ touch README.md
```
#### Task 3: Rename your main branch from master to main (If your branch name is already main then rename it to master and then back to main)
```bash 
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git branch --show-current
main
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git branch -m main master
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git branch --show-current
master
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git branch -m master main
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git branch --show-current
main
```
#### Task 4: Stage your changes and commit them
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git add .
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git commit -m 'Initial commit (Git Basics)'
[main (root-commit) d5268b1] Initial commit (Git Basics)
 1 file changed, 28 insertions(+)
 create mode 100644 README.md
```
#### Task 5: Create a Github repo and connect it with your project
```bash 
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git remote add origin https://github.com/Guhirwa/Git-Basis-cs.git
```
#### Task 6: Push your changes to Github
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 701 bytes | 350.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Guhirwa/Git-Basis-cs.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```
#### Task 7: Create a new branch dev
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git checkout -b dev
Switched to a new branch 'dev'
```
#### Task 8: From dev create another branch test
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git checkout -b test
Switched to a new branch 'test'
```
### Task 9: Go back to the dev branch and delete the test branch
```bash 
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git checkout dev
M       README.md
Switched to branch 'dev'
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git branch -d test
Deleted branch test (was d5268b1).
```

### Exercise 2
- Create a new `home.html` file, add some html changes and save them
```bash

```
- Stash save your current changes
```bash

```
- Repeat the same process for a new `about.html` page and stash save your changes
```bash

```
- Repeat the same process for a new `team.html` page and stash save your changes
```bash

```
- Using stash pop restore the changes of the `about.html` page
```bash

```
- With the help of an index use stash pop bring back the `home.html` page changes
```bash

```
- Commit the current changes and push them
```bash

```
- Using stash pop restore the changes of the `team.html` page index
```bash

```
- Reset the current changes using git reset and go back to the changes without the `team.html` page
```bash

```