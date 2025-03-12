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
hint: git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint: git branch -m <name>
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
* [new branch] main -> main
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
M README.md
Switched to branch 'dev'
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git branch -d test
Deleted branch test (was d5268b1).
```

### Exercise 2
- Create a new `home.html` file, add some html changes and save them
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ touch home.html
```
- Stash save your current changes
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git add home.html
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git stash save "Added hone.html"
Saved working directory and index state On dev: Added hone.html
```
- Repeat the same process for a new `about.html` page and stash save your changes
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ touch about.html
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git add about.html
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git stash save "Added about.html"
Saved working directory and index state On dev: Added about.html
```
- Repeat the same process for a new `team.html` page and stash save your changes
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ touch team.html
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git add . team.html
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git stash save "Added team.html"
Saved working directory and index state On dev: Added team.html
```
- Using stash pop restore the changes of the `about.html` page
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git stash list
stash@{0}: On dev: Added team.html
stash@{1}: On dev: Added about.html
stash@{2}: On dev: Added hone.html
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git stash pop stash@{1}
On branch dev
Changes to be committed:
(use "git restore --staged <file>..." to unstage)
new file: about.html

Dropped stash@{1} (66cf0bba055945a65f48b3557696e7612a33172d)
```
- With the help of an index use stash pop bring back the `home.html` page changes
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git stash list
stash@{0}: On dev: Added team.html
stash@{1}: On dev: Added hone.html
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git stash pop stash@{1}
On branch dev
Changes to be committed:
(use "git restore --staged <file>..." to unstage)
new file: about.html
new file: home.html

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: README.md

Dropped stash@{1} (7671d50d2b4b1a4749b71f4352b2be66dbc62b3f)
```
- Commit the current changes and push them
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git status
On branch dev
Changes to be committed:
(use "git restore --staged <file>..." to unstage)
new file: about.html
new file: home.html

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: README.md

guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git add .
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git status
On branch dev
Changes to be committed:
(use "git restore --staged <file>..." to unstage)
modified: README.md
new file: about.html
new file: home.html

guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git commit -m "Add update on README.md, and pushing about.html and home.html"
[dev 6e05dd9] Add update on README.md, and pushing about.html and home.html
3 files changed, 113 insertions(+)
create mode 100644 about.html
create mode 100644 home.html
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git branch --show-current
dev
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git push origin dev
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 2.03 KiB | 520.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote: https://github.com/Guhirwa/Git-Basis-cs/pull/new/dev
remote: 
To https://github.com/Guhirwa/Git-Basis-cs.git
* [new branch] dev -> dev
```
- Using stash pop restore the changes of the `team.html` page index
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git stash list
stash@{0}: On dev: Added team.html
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git stash pop stash@{0}
On branch dev
Changes to be committed:
(use "git restore --staged <file>..." to unstage)
new file: team.html

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: README.md

Dropped stash@{0} (3bc52c7448553e97dcf58e9852d0f72f30ac7a45)
```
- Reset the current changes using git reset and go back to the changes without the `team.html` page
```bash
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git reset
Unstaged changes after reset:
M README.md
```

## Bundle 2
### Exercise 1
- Create a new branch named `ft/bundle-2`
```bash 
guhirwa@Thinkpad-Linux-X270:~/Documents/Selfpace/The Gym/Git Basics$ git checkout -b ft/bundle-
2
Switched to a new branch 'ft/bundle-2'
```
- Add new changes to your project. create a new page named `services.html` and add some changes
```bash 

```
- Commit your changes and create a Pull Request against the `main` branch in your github repository
```bash 

```
- Request a review and make sure your Pull request gets merged (Look for someone to merge your PR)
```bash 

```
