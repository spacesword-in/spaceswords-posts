title: Git Tutorial
author: Amit Chambial
tags:
  - GIT
categories:
  - Open Source
  - GIT
date: 2017-11-13 06:26:00
---
<!--Gitub Tutorial-->
![git](https://git-scm.com/images/logos/downloads/Git-Logo-1788C.png)
## Setup
### For Windows :
[Download Git Bash For Windows](https://github.com/git-for-windows/git/releases/tag/v2.13.0.windows.1)
### For Mac Os :
[Download Git For Mac](https://sourceforge.net/projects/git-osx-installer/files/git-2.13.0-intel-universal-mavericks.dmg/download?use_mirror=autoselect)
### For Linux :
If you want to install the basic Git tools on Linux via a binary installer, you can generally do so through the basic package-management tool that comes with your distribution. If you’re on Fedora for example, you can use yum:
```shell
    $ sudo yum install git-all
```
If you’re on a Debian-based distribution like Ubuntu, try apt-get:
```shell
    $ sudo apt-get install git-all
```
For more options, there are instructions for installing on several different Unix flavors on the Git website, at http://git-scm.com/download/linux.
## Create a new repository
create a new directory, open it and perform a
<code>git init</code>
to create a new git repository.
## add & commit
You can propose changes (add it to the Index) using
```shell
    git add <filename>  
    git add *
```
to add whole directory: 
```
    git add .
    git add --all
```
This is the first step in the basic git workflow. To actually commit these changes use
```
    git commit -m "Commit message"
    ```
Now the file is committed to the HEAD, but not in your remote repository yet.
## Pushing Changes

Your changes are now in the HEAD of your local working copy. To send those changes to your remote repository, execute
```
    git push origin master
```
Change master to whatever branch you want to push your changes to.

If you have not cloned an existing repository and want to connect your repository to a remote server, you need to add it with
```
    git remote add origin <server>
```
Now you are able to push your changes to the selected remote server
## update & merge
To update your local repository to the newest commit, execute
```
    git pull
```
in your working directory to fetch and merge remote changes.
to merge another branch into your active branch (e.g. master),use
```
    git merge <branch>
```
in both cases git tries to auto-merge changes. Unfortunately, this is not always possible and results in conflicts. You are responsible to merge those conflicts manually by editing the files shown by git. After changing, you need to mark them as merged with
```
    git add <filename>
```
before merging changes, you can also preview them by using
```
    git diff <source_branch> <target_branch>
```
## Adding a remote
To add a new remote, use the git remote add command on the terminal, in the directory your repository is stored at.

The git remote add command takes two arguments:

    A remote name, for example, origin
    A remote URL, for example, https://github.com/user/repo.git

For example:
```
    git remote add origin https://github.com/user/repo.git
```
### Set a new remote
```
    git remote -v
```
### Verify new remote
   ```
   origin  https://github.com/user/repo.git (fetch)
   origin  https://github.com/user/repo.git (push)
   ```
