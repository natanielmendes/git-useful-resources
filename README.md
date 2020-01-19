# Useful Resources to Git

## How I would Setup Git
```
$ git config --global user.name "Nataniel Carvalho"
$ git config --global user.email "natanielmendes@hotmail.com"
$ git config --global color.ui "auto"
```
https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup

## Associating VS Code as default text editor to Git
```
$ git config --global core.editor "code --wait"
```
https://help.github.com/en/github/using-git/associating-text-editors-with-git]

## Best practices related to commit messages
https://udacity.github.io/git-styleguide/

## Basic Merge Conflicts from the Git book
https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging#Basic-Merge-Conflicts

## How Conflicts Are Presented from the Git docs
https://git-scm.com/docs/git-merge#_how_conflicts_are_presented

## How to revert a commit
```
$ git revert <SHA-of-commit-to-revert>
```
https://www.atlassian.com/git/tutorials/undoing-changes

## Relative Commit References
### The parent commit – the following indicate the parent commit of the current commit
```
HEAD^
HEAD~
HEAD~1
```
### The grandparent commit – the following indicate the grandparent commit of the current commit
```
HEAD^^
HEAD~2
```
### The great-grandparent commit – the following indicate the great-grandparent commit of the current commit
```
HEAD^^^
HEAD~3
```
### The 4th parent commit – the following indicate the 4th parent commit of the current commit
```
HEAD^^^^
HEAD~4
```

## Resetting one commit
### When you want to reset the last commit, placing it to the Working Directory, run:
```
git reset HEAD~1
```
### OR:
```
git reset --mixed HEAD~1
```
### When you want to reset the last commit, placing it to the Staging Index, run:
```
git reset --soft HEAD~1
```
### When you want to reset the last commit throwing it to trash, run:
```
git reset --hard HEAD~1
```
### When working with RESET, don't forget to create a backup branch
```
git branch backup
```

## Working with remotes
### Git book reference
https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes#_showing_your_remotes

### 'git remote' command from Git Docs 
https://git-scm.com/docs/git-remote

## Reviewing Existing Work
### Group By Commit Author
```
git shortlog
```
### Group By Commit Author to display commit count ordered by commit quantity
```
git shortlog -s -n
```
### Filter By Author with name starting by "Surma"
```
git log --author=Surma
```
### See extra detils of a commit
```
git log --author=Surma
```
### Filtering commits by descriptive message
```
git log --grep=bug
```
```
git log --grep bug
```
## In order to change remote branch
### Remove current origin
```
git remote rm origin
```
### Add new origin
```
git remote add origin https://github.com/natanielmendes/my-travel-plans.git
```
## Rebasing commits
### interactive rebase
```
$ git rebase -i <base>
```
### interactively rebase the commits to the one that's 3 before the one we're on
```
$ git rebase -i HEAD~3
```
### Rebasing commands
```
use p or pick – to keep the commit as is
use r or reword – to keep the commit's content but alter the commit message
use e or edit – to keep the commit's content but stop before committing so that you can:
add new content or files
remove content or files
alter the content that was going to be committed
use s or squash – to combine this commit's changes into the previous commit (the commit above it in the list)
use f or fixup – to combine this commit's change into the previous one but drop the commit message
use x or exec – to run a shell command
use d or drop – to delete the commit
```
## The best way to become a Git Beast is from collaborating with others
http://up-for-grabs.net/#/
http://www.firsttimersonly.com/
https://github.com/search?utf8=%E2%9C%93&q=label%3Afirst-timers-only+is%3Aopen&type=Issues&ref=searchresults
https://github.com/jlord/git-it-electron