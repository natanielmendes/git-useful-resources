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

