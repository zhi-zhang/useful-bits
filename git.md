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

## Useful Commands
> "When in trouble, read the frickn' [manual](https://git-scm.com/docs/user-manual)."

The following is based on [github git handbook](https://guides.github.com/introduction/git-handbook/).

* `git init` initializes a brand new Git repository and begins tracking an existing directory. 
It adds a hidden subfolder within the existing directory that houses the internal data structure required for version control.

* `git clone` creates a local copy of a project that already exists remotely. 
The clone includes all the project’s files, history, and branches.

* `git add` stages a change. Git tracks changes to a developer’s codebase, 
but it’s necessary to stage and take a snapshot of the changes to include them in the project’s history.
This command performs staging, the first part of that two-step process.
Any changes that are staged will become a part of the next snapshot and a part of the project’s history.
Staging and committing separately gives developers complete control over the history of their project
without changing how they code and work.

* `git commit` saves the snapshot to the project history and completes the change-tracking process.
In short, a commit functions like taking a photo. 
Anything that’s been staged with git add will become a part of the snapshot with git commit.

* `git status` shows the status of changes as untracked, modified, or staged.

* `git branch` shows the branches being worked on locally.

* `git merge` merges lines of development together. 
This command is typically used to combine changes made on two distinct branches. 
For example, a developer would merge when they want to combine changes from a feature branch into the master branch for deployment.

* `git pull` updates the local line of development with updates from its remote counterpart.
Developers use this command if a teammate has made commits to a branch on a remote,
and they would like to reflect those changes in their local environment.
  
* `git push` updates the remote repository with any commits made locally to a branch. 
  * `-u` / `--set-upstream` : For every branch that is up to date or successfully pushed, add upstream (tracking) reference.


* Add an upstream repository: `git remote add {local_nickname} {repository_url}`
* Push to a specific upstream repository: git push {local_nickname} {branch}

### Shortcut to avoid having to type in login detail every time
Chose one of the following option. 

1. [Store git credential](https://git-scm.com/docs/git-credential-store) : `git config credential.helper store`
1. [Cache git credential](https://git-scm.com/docs/git-credential-cache) : `git config credential.helper cache`
1. [Setup SSH key](https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)

**Note: For option 1 and 2, it is applied per repository, use `--global` option save  the config for all repository of the user. `--system` apply the setting for all user of a computer.  
