# GitTreasure
# Git

Git is a distributed version-control system for tracking changes in source code during software development. Below are all the must know git commands from begining to advance level.

[![Build Status](https://img.shields.io/badge/Git-A%20Stupid%20Content%20Tracker-red)](https://git-scm.com/docs/git)

## Git Setup
To take benefits of Git you first need to intall it.

#### Installing on Linux
```sh
Fedora - $ sudo dnf install git-all
or
Ubuntu - $ sudo apt install git-all
```

[All Other options](https://git-scm.com/download/linux)

#### Installing on Mac
```sh
Homebrew - $ brew install git
```
[All Other options](https://git-scm.com/download/mac)

#### Installing on Windows
[Download from Git wesite.](https://git-scm.com/download/win)

### User Configuration
```sh
$ git config --global user.name "user name"
$ git config --global user.email "user email"
```

## Repository
A Git repository is nothing but a directory under version control. You typically obtain a Git repository in one of two ways:
* You can take a local directory that is currently not under version control, and turn it into a Git repository, or
* You can clone an existing Git repository from elsewhere.

In either case, you end up with a Git repository on your local machine, ready for work.

Create Repository
```sh
$ cd <path-to-project>
$ git init
```
Clone Remote repo
```sh
$ git clone <remote-repo-URL>
```
File Tracking LifeCycle
![Image](img/fileTrackingLifeCycle.png)

## Git Commands
* Current branch 
    ```sh
        $ git branch
    ```
* Current changes 
    ```sh
        $ git status
    ```
 * Git history
    ```sh
        $ git log
    ```
* Commit : A commit in a git repository records a snapshot of all the files in your directory.
    ```sh
        $ git commit -m "Commit Message"
    ```
* Branching
    * create branch
        ```sh 
            $ git branch <branch-name>
        ```
    * checkout on branch
        ```sh 
            $ git checkout <branch-name>
        ```
    * create and checkout on branch
        ```sh 
            $ git checkout -b <branch-name>
        ```
* Stage changes
    * All Changes
        ```sh 
            $ git add .
        ```
    * Particular file
        ```sh
            $ git add <file-name>
        ```
* Unstage changes
    * Unstage one file
        ```sh
            $ git checkout <path-to-file>
      ```
    * Unstage all files
        ```sh 
            $ git checkout -- .
        ```
* Remove un-staged file
    * remove folder directory 
        ```sh 
            $ git clean -f -d 
            or
            $ git clean -fd
        ```
    * remove ignored files 
        ```sh 
            $ git clean -fX
        ```
    * remove ignored and no-ignored files 
        ```sh 
            $ git clean -fx
        ```
* Reset uncommitted changes
    * Un-staged changes 
        ```sh 
            $ git checkout — <file-name>
        ```
* Merge: Steps to merge branchFoo into branchBar
    ```sh 
        $ git checkout branchBar 
        $ git merge branchFoo
    ```
* Cherry-Pick
    ```sh 
        $ git cherry-pick <commit1> <commit2> … <commitN>
    ```
* Rebase
    ```sh 
        $ git rebase <branch-name-to-be-rebased-in-current-branch>
    ```
