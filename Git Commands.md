***
Git Commands
***


#Globals
##Set global variables
git config --global user.name "Phil Kaufman"
git config --global user.email "pkaufman9966@gmail.com"
##list global variables
git config --list

#Init local repo
git init

#Clone
git clone https://github.com/pkaufman9966/HelloWorld.git

#Working tree
##undo working tree file with version from staging area
git checkout -- <filename>

#Staging area
##add files to staging (index) area
git add README.md 
git add "Git Commands.md"
get add .
##diff working tree diff vs staging (index) area
git diff
##undo staged file change with version from commit
git reset HEAD <filename>
##restore file from earlier commit (into staging AND working tree)
git checkout <commithash> -- <filename>

#Commits
##status
git status
##Commiting
git commit -m "Add readme and git commands files"
git commit
##commit graph
git log
git log -p
git log -- <filename>
##diff staging (index) area vs history
git diff --staged
##restore commited file
