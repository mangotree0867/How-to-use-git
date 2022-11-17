# How-to-use-git
This is my own cheat sheet for how to use git / git-hub
You can always ask git for help with commands!! 
        -> git help / git [command] -h / git help [command]

What is git : it is Source Control Management(SCM) system that you can use to keep track of your work. It is mainly used to work on projects in your local workspace.

Configuring Git :
 - Why we need to configure git : we need to do this so that we know who is making changes to the workspace.
- setting user name :         git config --global user.name "First_name Last_name"
- setting email address :     git config --global user.email abcdefg@gmail.com
- setting branch :            git config --global init.default branch main

To create repository for a folder :
- go to the path(folder) that you want to make a repository of and then type  :     git init
-> you can see that it is made by seeing the hidden files in the file explorer

To check the status of git : git status

To track files : 
 - to track one file :                       git add [file_name_to_track.cpp]
 - to track all the files in the path :      git add . (or git add --all)
Tracking the files makes the status of the file to staging so that git can keep track of the changes made before commiting
 - to remove the file from staging status :  git restore --staged [name_of_file_to_remove_from_staging] -> goes back to the working files

To untrack a file : git rm --cached [file_name_to_untrack.cpp]

To ingnore certain files in git :
- you can create a file called .gitignore and type in the files that you want to ignore
eg) *.txt, *.cpp

What is commiting?? - commiting is basically taking a screenshot of your repository at this point of time
To make a commit (from staging) : 
 - git commit -m "[message to go with commit]"
To make a commit directly (skips staging) :
  - git commit -a -m "[message to go with commit]"
 
To check the differences made compared to the previous version : git diff
 
To delete file : git rm "[name_of_file_to_delete]"
To restore file : git restore "[name_of_the_file_to_restore]"
 
To review all the commits we made :                         git log [-p] ( the -p option allows you to see the specific details of the log )
To change the commit message after commit has been made :   git commit -m "[message]" --amend
To jump to a previous commit stage :                        git reset [hashtag of the commit]
To change the commit log :                                  git rebase -i --root
 
What is a branch : a copy of the main branch - allows you to work on different features so that you can collaborate without changing the main branch - after you finish making changes to the other branch you can merge it to the main branch

To create a new branch :                  git branch [name_of_branch_to_make]
To change the current working branch :    git switch [name_of_branch_to_change_to]
To see branches :                         git branch
To delete branch :                        git branch -d [name_of_branch_to_delete]

To merge branches back to main: git merge -m "[message_to_write]"

merge conflict : when you try to merge a branch you fixed back to main but the part you have change has been modified too
-> you need to choose with part you are going to keep
-> you will see that you are in MERGING mode when this happens

HEAD : the part that is in main
[branch_name] : the part that you are trying to merge

