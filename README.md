# GIT EXERCISES
## Bundle 1
### Exercise 1
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
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ touch README.md
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git branch --show-current
main
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git branch -m main master
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git branch --show-current
master
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git branch -m master main
guhirwa@Guhirwa-ThinkPad-X270:~/Documents/The Gym/Git Basics$ git branch --show-current
main
```