# Git

## Setting up Git: -
1. git init

2. git config user.name "someone"

3. git config user.email "someone@someplace.com"

4. git add *

5. git commit -m "some init msg"

## Commands: -


1.) **`git clone`** - Takes a repository and store it somewhere else like on a server like GitHub

Syntax: `git clone repository_url`

2.) **`git add`** - Take one or more files that have been changed and tell git that these are the files that need to be added the next time we make a commit

Syntax: `git add filename`

3.) **`git commit`** - Take the snapshot of the repo at the current moment and save it

Syntax: `git commit -m "message"`

To add and commit at the same time : `git commit -am "message"`

4.) **`git status`** - What's currently going on in the repo

5.) **`git push`** - push our code from the local repo to the GitHub

6.) **`git pull`** - Download the latest version of the repository

Essentially (git fetch + fast forward)


Merge Conflicts - When two developers have commited the same file.

Anything between <<<<< and ==== are the changes made by you on the local system 
Anything between ==== and >>>> are the changes made by another developer on a remote system

7.) **`git log`** - log of the stuff happening

8.) **`git reset`** - Get rid of the changes

Syntax:
`git reset --hard <commit>`
`git reset --hard origin/master`

9.) **`git branch`** - List of all the branches in the repository

Syntax to create a new branch:
`git branch branch_name`

10.) **`git checkout`** - Switch to another branch

Syntax: `git checkout branch_name`

11.) **`git merge`** - Merge two branches

12.) **`git push`** --set-upstream origin name_of_the_branch - Push from local computer to GitHub

13.) **`git config --global pull.rebase true`**

14.) **`git config credential.helper cache`**


Daemon Command: git daemon

Serve Alias: git config --global alias.serve "daemon --verbose --export-all --base-path==git --reuseaddr --strict-paths--enable=receive-pack.git/

Clone Command: git clone git://yourmachine/path/to/repo


## Working with Git Large File Storage (LFS)

Download and install Git LFS from [here](https://git-lfs.github.com/)

1.) Setting up Git LFS - `git lfs install`

This need to be run from the repository directory.

2.) Select the file types you'd like Git LFS to manage - `git lfs track "*.psd"`
Make sure .gitattributes is tracked using - `git add .gitattributes`

3.) Commit and push to GitHub - 

`git add file.psd`
`git commit -m "Some comment which describes your addition"`
`git push origin master`
