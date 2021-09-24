Git Commands
============

Let's document some git commands in markdown!

Motivation
----------

It's always nice to kill two birds with one stone.  Learn git, learn md.

Installation
------------

Nothing to install

The GIT Language and Commands
--------

### Globals

#### Set global variables
```
$ git config --global user.name "Phil Kaufman"
$ git config --global user.email "pkaufman9966@gmail.com"
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
$ git checkout -- {file name}
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
$ git reset HEAD {filename}
```

#### restore file from earlier commit (into staging AND working tree)
```
$ git checkout {commithash} -- {filename}
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

#### commit graph
```
$ git log
$ git log -p
$ git log -- {filename}
```

#### diff staging (index) area vs history
```
$ git diff --staged
```

### Branch

