Log in to GITHub with my credentials
Create New Repo: ARIES
Create ARIES folder in path: C:\Users\rijjeje\ARIES from my local laptop
Create reaadme file in there
Will now save this doc and push it to remote repository - ARIES

Initialised the Repo
Added the file
Committed the file

===========================
git remote add origin git@github.com:rijjeje/ARIES.git
##if origin gives error use github to replace origin
git push -u origin master
#if origin gives error use github to replace origin
This should prompt for userid and password to your account on github
On providing the same, it will push the local repo to the master branch in github
============================

Then create 2 branches from master
git checkout –b Release
git push -u github Release

git checkout –b prodsupport
git push -u github prodsupport

This creates total 3 branches on remote – Master, Release and prodsupport all with the same content of a readme file.

=============================

Now created a local folder : C:\Users\rijjeje\Release
cloned the Release branch into this Release folder
git clone -b Release https://github.com/rijjeje/ARIES.git

Then made this changes to Read mefile.

Now will check this in to remote, whichs houd effectively update the Release branch on server 
However the readme file in Master and prodsupport branches should not show the changes
---------------------------------

To check in get into the ARIES folder within local Release workspace
Git add .
Git commit –m “all”
Git push –u origin Release (replace origin by github if you encounter error)

Now we will merge remote brnch release into 1. Prodsupport and 2. Master. To do so:
1.	Get into the local prodsupport folder
2.	Git checkout prodsupport
3.	Git merge Release
4.	This will bring all updates from remote Release branch to local prodsupport workspace
5.	Now, git push –u origin prodsupport. This will push the local prodsupport updates into remote prodsupport
Follow similar steps to update master branch with Release branch updates

At this stage all the three branches – Master, Release and prodsupport are synched.


For an outdated local workspace to be updated from remote, use:

Git pull origin <Remote branch> Remote branch can be – master/Release/prodsupport



