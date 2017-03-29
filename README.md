# LocalSourceControl
Simple deployment of a private git solution for professional teams

## Automatic Method 

Run the following scripts ............

## Manual Method 

### First Configure a New Repository on any Local Server:

1) On the server create a directory for all git projects to be stored `mkdir projectdirectory`
2) cd into the directory `cd projectdirectory`
3) Initialize git by typing `git init`



### Create SSH Keys for passwordless login:

1) Type ssh-keygen -t rsa
2) Type `cat ~/.ssh/id_rsa.pub | ssh speech@192.168.100.125 "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys"`

### Initial Setup:

1) First go to a new directory on your computer which will be your working directory
2) Run the following command: `git clone speech@192.168.100.125:/home/speech/git/projects.git`
3) Cd into the Projects Directory `cd Projectdirecotry`
4) Create a new Branch and Name it something that describes the changes you are making for example "Fixed VAD" : `git branch $branchname$`
5) Move to your branch by typing `git checkout $branchname$`
6) Make sure you are in the new branch by typing `git status`
7) Once you know you are in the new branch, start changing the files there normally, and use this directory for all the work
8) Once you have finished making changes , type git add . for these changes to be updated.
9) Check the differences between master branch and your branch by typing git diff , make sure the changes have been reflected here
10) Now its time to commit , type git commit -m CommitName , here CommitName describes any issues you have fixed
11) Finally its time to push your changes to origin. Type git push origin Branchname
12) Wait for admin to accept your commit and merge your branch to the master.
13) Have fun!

### Daily Usage:

1) First, fetch all the changes made while others were working on the project by typing git pull
2) Next start a new branch for whatever changes you will be making for example SRTfix , git branch branchname
3) Double check that you are on a new branch by typing git status
4) Continue working as usal and when you are done do git add .
5) Check if the changes have been reflected by typing git diff
6) Commit the changes by typing git commit -m CommitName , here commitname describes what problems you may have solved
7) Now its time to push your changes , type git push origin BranchName
8) Wait for admin to merge
9) Have fun!
