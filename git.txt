------------------------------------	Git setup commands  ------------------------------------

git config --global user.name <username>            -->   Add username
git config --global user.email <user_email_id>      -->   Add emailid

git init                                            -->   Add tracker to the folder
rm -rf .git                                         -->   Remove tracker from the folder

git clone <URL> <where to clone>                    -->   Cloning a remote repository
git remote -v                                       -->   Shows info of the original repository




------------------------------------	Difference commands  ------------------------------------

git diff            -->     Shows changes made in the files
git status          -->     Shows untracked and tracked files
git log             -->     Shows the commit logs
git log -p          -->     Shows all the changes made in the repo




------------------------------------	Stagging commands  ------------------------------------

git add *                           -->     Adds untracked files
git checkout <file_name>            -->     Revert changes to modified files before they are staged
git reset HEAD <file_name>          -->     Removes files from staging area




------------------------------------	Commit commands  ------------------------------------

git show                        -->     Returns a list of commits andd commit id made in the repo
git show <commit-id>            -->     Shows the changes made in the repo at that commit
git commit -m "message"         -->     Commits the changes
git commit -a -m  "message"     -->     Stages files automatically and commits the changes
git commit --amend              -->     Overwrite the previous commit




------------------------------------	Rollback commands  ------------------------------------

git revert HEAD	                -->     makes a new commit which effectively rolls back a previous commit. It’s a bit like an undo command.
git revert HEAD^                -->     reverts back to last commit while keeping the changes
git checkout HEAD~X             -->     Here X is the number of comits to go back to
git revert <commit-id>	        -->     roll back to the time where the specified commit was made with a new commit to the the repo




------------------------------------	Update to Github commands  ------------------------------------

git pull origin master              -->     Updates changes from the repo
git push origin master              -->     Updates to the remote repo
git push --force origin master      -->     Force update the remote repo




------------------------------------	Braching and merging commands  ------------------------------------

git branch                      -->   Shows all the branches 
git branch -a                   -->   Shows all the branch of the original repository
git branch <branch_name>        -->   Creates a new branch
git branch -d <branch_name>     -->   Deletes a local repo branch
git branch -D <branch_name>     -->   Forcibly deletes the branch

git checkout <branch_name>      -->   Changes the branch
git checkout -b <branch_name>   -->   Create a new branch and change to that branch

git branch --merged             -->   Shows all the branches we have merged
git merge <branch_name>         -->   Merges branch to the current branch
git merge --abort               -->   If there are merge conflicts (meaning files are incompatible), --abort can be used to abort the merge action

git push -u origin <branch_name>            -->   Creates branch in remote repo
git push origin --delete <branch_name>      -->   Deletes a remote repo branch

git rebase <origin_branch_name>         -->     Rebase the origin branch from where the current branch is generated
git rebase --continue                   -->     continue rebase process
