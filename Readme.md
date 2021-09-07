I. Create a new repository
--------------------------
1) git init
 * start new repository for the current folder (?)

II. Stage files - prepare files to be commited
----------------------------------------------
2) git add Readme.md
 * add file(s) or folder(s) to be staged

III. Commit files to local repository
-------------------------------------
3) git status
 * see staged files awaiting to be commited

4) git commit -m "first commit"
 * commit staged files with -m "message"

IV. Setup GitHub repository
---------------------------
5) git branch -M main_branch
 * sets main_branch as the root, main or master branch; CAREFUL!

6) git remote add origin git@github.com:userName/repositoryName.git
 > git remote add origin git@github.com:tomasfn87/learningGit.git
 * add the URL for the destination repository as alias "origin"
1
7) git remote -v
 * show remote URL for fetch/push operations; can be altered by step 8

V. Add authentication token
---------------------------
Get your token:
> github.com > Settings > Developer settings > Personal access tokens > Generate new token
8) git remote set-url origin https://ghp_y1gKcGkUeIMRgGoxp0Ztk_your_token_tS@github.com/username/repository_name.git
 > git remote set-url origin https://(-------------your----token-----------)@(--------------clone-URL--------------)
 * change the remote repository URL for fetch and push operations

VI. Push local files to github.com repository
---------------------------------------------
9) git push -u origin main
 > git push origin main
 * push/send files to repository; option -u is required only the first time
 * will prompt for username and password (password is view-safe on WSL 2, at least)

VII. To fetch files that exist only in the github repository to your local folder
----------------------------------------------------------------------------------
10) git pull origin main --allow-unrelated-histories
 * sometimes you must pull files from github before pushing from local repository
 * --allow-unrelated-histories helps your merge local and git files

IX. To create and switch to a new branch (and back) and to merge branches
-------------------------------------------------------------------------
11) git checkout -b "new-button"
 * leaves actual branch and creates a new branch named "new-button"
 > git checkout "main"
 * leaves actual branch and goes to the existing "main" branch
 > git checkout "new-button"
 * leaves actual branch and foes to the existing "new-button" branch
 
12) git branch (--list) 
 * shows a list of branches; the actual branch will be green and marked with an asterisk (*)

13) (git branch) (git checkout "main") git merge new-button
 * While in main (check with git branch and switch branches with gut checkout "branch_name"), merge new-button's and main's files, that can then be uploaded to the repository with git add . && git commit -m "message"

14) git clone URL
  > git clone https://github.com/tomasfn87/learningGit.git
 * Downloads the specified repository URL to your local directory to a folder named 'repository-name': 'learninGit'

 15) > git restore file... 
   * Revert a file to an earlier version stored locally
 
   > git restore --staged file...
   > git rm --cached file...
   * To unstage files that are awaiting to be commited (git add)
   
   > git rm -f file...
   * To force removal of files that were staged and are awaiting to be commited
   
   
