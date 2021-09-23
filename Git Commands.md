



#Clone
git clone https://github.com/pkaufman9966/HelloWorld.git

#Globals
##Set global variables
git config --global user.name "Phil Kaufman"
git config --global user.email "pkaufman9966@gmail.com"
##list global variables
git config --list

#Staging area
##add files to staging (index) area
git add README.md 
git add "Git Commands.md"
get add .
##diff working tree diff vs staging (index) area
git diff

#Commits
##status
git status
##Commiting
git commit -m "Add readme and git commands files"
##commit graph
git log
##diff staging (index) area vs history
git diff --staged
