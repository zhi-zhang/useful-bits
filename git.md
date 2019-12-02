# Git 

## Setup

Chocolatey command: `choco install git`

[Direct download](https://git-scm.com/downloads)


## Tutorials

* [Interactive https://learngitbranching.js.org/](https://learngitbranching.js.org/)
* [Atlassian](https://www.atlassian.com/git)
* [Github](https://try.github.io/)
* [Git manual](https://git-scm.com/docs/user-manual)
* [Pro Git book](https://git-scm.com/book/en/v2)
* [Some reading of rebasing](https://devblogs.microsoft.com/oldnewthing/20180323-01/?p=98325)

## Useful Commands
>"Remember to keep calm and read the frickn' [manual](https://git-scm.com/docs/user-manual)"

The following is based on [github git handbook](https://guides.github.com/introduction/git-handbook/).

* [`git help`](https://git-scm.com/docs/git-help) will show a list of common commands. 
Use `-h` or `--help` to lookup documentation of commands.

* [`git init`](https://git-scm.com/docs/git-init)
initializes a brand new Git repository and begins tracking an existing directory. 
It adds a hidden subfolder within the existing directory that houses the internal data structure required for version control.

* [`git clone`](https://git-scm.com/docs/git-clone)
creates a local copy of a project that already exists remotely. 
The clone includes all the project’s files, history, and branches.

* [`git branch`](https://git-scm.com/docs/git-branch)
shows the branches being worked on locally.
  * `--remotes`: List or delete (if used with -d) the remote-tracking branches. 
  * `--all` : List both remote-tracking branches and local branches. 
  Combine with --list to match optional pattern(s).
  * `--move` : Move/rename a branch and the corresponding 
  [reflog](https://www.atlassian.com/git/tutorials/rewriting-history/git-reflog).
  * `--delete` : Delete a branch. 
  The branch must be fully merged in its upstream branch,
  or in HEAD if no upstream was set with `--track` or `--set-upstream-to`.
  * `--delete --force`.
  * `--set-upstream-to=<upstream>` : 
  Set up <branchname>'s tracking information so <upstream> is considered <branchname>'s upstream branch. 
  If no <branchname> is specified, then it defaults to the current branch.
  * `--unset-upstream` :
  Remove the upstream information for <branchname>. If no branch is specified it defaults to the current branch.
  * `--track` : When creating a new branch, set the branch to track a remote repository. 
  E.g.: `git branch {branch_name} --track {origin/branch_name}`
  
* [`git add <pathspec>`](https://git-scm.com/docs/git-add)
stages a change. Git tracks changes to a developer’s codebase, 
but it’s necessary to stage and take a snapshot of the changes to include them in the project’s history.
This command performs staging, the first part of that two-step process.
Any changes that are staged will become a part of the next snapshot and a part of the project’s history.
Staging and committing separately gives developers complete control over the history of their project
without changing how they code and work.
 * '--all' : update all files in the entire working tree.
 
* [`git commit`](https://git-scm.com/docs/git-commit)
saves the snapshot to the project history and completes the change-tracking process.
In short, a commit functions like taking a photo. 
Anything that’s been staged with git add will become a part of the snapshot with git commit.
 * `--message=<msg>` : add message as commit message.
 If multiple `-m` options are given, their values are concatenated as separate paragraphs.
 * `--all` : 
 Tell the command to automatically stage files that have been modified and deleted, 
 but new files you have not told Git about are not affected.

* [`git status`](https://git-scm.com/docs/git-status)
shows the status of changes as untracked, modified, or staged.

* [`git merge`](https://git-scm.com/docs/git-merge)
merges lines of development together. 
This command is typically used to combine changes made on two distinct branches. 
For example, a developer would merge when they want to combine changes from a feature branch into the master branch for deployment.

* [`git pull`](https://git-scm.com/docs/git-pull)
updates the local line of development with updates from its remote counterpart.
Developers use this command if a teammate has made commits to a branch on a remote,
and they would like to reflect those changes in their local environment.
  
* [`git push`](https://git-scm.com/docs/git-push)
updates the remote repository with any commits made locally to a branch. 
  * `--set-upstream` : For every branch that is up to date or successfully pushed, add upstream (tracking) reference.

* [`git rebase`](https://git-scm.com/docs/git-rebase)
Change the base of the branch to make it appear as if it was created base on another commit. **This is rewriting history and can be dangerous.  You should never rebase commits once they've been pushed to a public repository. Take care when you are working on a "semi-public" repository (ie when your private branch can be accessed remotely".**
 * `--interactive` : 
 Make a list of the commits which are about to be rebased. 
 Let the user edit that list before rebasing. 
 Useful for compact and clean up git history.
 
 * [`git stash`](https://git-scm.com/docs/git-stash)
 store the current changes and restore the working directory to previous commit state.
  * `apply` : apply a single stashed state from the stash list on top of the current working tree state.
  * `drop` : Remove a single stash entry from the list of stash entries. 
  * `pop` : `apply` + `drop`, note apply can fail.
  * `clear` : Remove all the stash entries.

* Add an upstream repository: `git remote add {local_nickname} {repository_url}`
* Push to a specific upstream repository: git push {local_nickname} {branch}

### Shortcut to avoid having to type in login detail every time
Chose one of the following option. 

1. [Store git credential](https://git-scm.com/docs/git-credential-store) : `git config credential.helper store`
1. [Cache git credential](https://git-scm.com/docs/git-credential-cache) : `git config credential.helper cache`
1. [Setup SSH key](https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)

**Note: For option 1 and 2, it is applied per repository, use `--global` option save  the config for all repository of the user. `--system` apply the setting for all user of a computer.  


### Change editor
>"Becausing `vim` is diffcult to learn"

On Windows using notepad++:

```
$ git config --global core.editor "'C:/Program Files (x86)/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"
```

[For other os](https://help.github.com/en/github/using-git/associating-text-editors-with-git)
