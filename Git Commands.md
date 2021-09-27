Git Commands
============

Let's document some git commands in markdown!

Readme
------

Please read this repository's readme file at:  `~/README.md`


Motivation
----------

It's always nice to kill two birds with one stone.  Learn git, learn md.

Installation
------------

Nothing to install

Use
---

Choose your favourite linux prompt like `bash` or `bourne`, or IDE tools like `VS Code` has embedded terminals, and enter git commands followed by pressing enter.

The GIT Language and Commands
--------

### Globals

#### Set global variables
```
$ git config --global user.name "<first name> <last name>"
$ git config --global user.email "email@address.com"
```

#### list global variables
```
$ git config --list
```

### Init - local repo
```
$ git init
```

### Clone
```
$ git clone https://github.com/pkaufman9966/HelloWorld.git
```

### WORKING TREE

#### undo working tree file with version from staging area
```
$ git checkout -- <file name>
```

### STAGING (INDEX) AREA

#### add files to staging (index) area
```
$ git add README.md
$ git add "Git Commands.md"
$ get add .
```

#### diff working tree diff vs staging (index) area
```
$ git diff
```

#### undo staged file change with version from commit
```
$ git reset HEAD <filename>
```

#### restore file from earlier commit (into staging AND working tree)
```
$ git checkout <commithash> -- <filename>
```
### HISTORY / COMMITS

#### status
```
$ git status
```

#### Commiting
```
$ git commit -m "Add readme and git commands files"
$ git commit
```

#### Stage and Commiting
```
$ git commit -a -m "Add readme and git commands files"
```


#### commit graph
```
$ git log
$ git log -p
$ git log -- <filename>
$ git log --all --decorate --oneline --graph
```

#### diff staging (index) area vs history
```
$ git diff --staged
```

### Branch
A `branch` is pointer to a SHA1 hash or commit.<br/>
Git creates a default branch called `master` when a repo is created.
The current (`HEAD`) branch pointer will advance with every commit.

#### Show branches
```
$ git branch
```
#### Show merged branches
```
$ git branch -- merged
```
#### Create new branch
```
$ git branch <branch name>
```
#### Delete new branch
```
$ git branch -d <branch name>
```

### Head
`HEAD` is a pointer (symbolic pointer) that points to a `branch`.<br/>
`HEAD` tells us what we have checked out.

#### Move `HEAD` pointer to a different branch
```
$ git checkout <branch name>
```

#### create and move `HEAD` pointer to a different branch
```
$ git checkout -b <branch name>
```

### Merge

#### see differences between two branches

```
$ git diff <branch1>..<branch2>
```
#### Fast Forward Merge

This happens when clear path from `master` to branch1.  No commit is created, branch1 pointer now points to a `master`.

#### 3-Way Merge / Merge Commit

This happens when there is no clear path from branch1 to `master`.<br/>
A new commit is created on with merged files.

```
git merge <branch1>
```

### Stash

Stash is like a snapshot of the current `working directory` and `staging area` that we can get back aty a later time.

#### see existing stashes
```
$ git stash list
```
#### Stash current changes
```
$ git stash save "<message">
```
#### Review changes in stash
```
$ git stash -p
```
#### Restore current stash over current state
```
$ git stash -apply
```

### Remotes

Remote is any non-local repository.

#### Remote status
```
$ git remote -v
```
#### Adding a remote to local repo
```
$ git remote add origin <repo url>
```


