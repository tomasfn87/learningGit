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
5) git branch -M main
 * specify the branch to be pushed (?)

6) git remote add origin git@github.com:userName/repositoryName.git
 > git remote add origin git@github.com:tomasfn87/learningGit.git
 * add the URL for the destination repository as alias "origin"

7) git remote -v
 * show remote URL for fetch/push operations; can be altered by step 8

V. Add authentication token
---------------------------
Get your token:
> github.com > Settings > Developer settings > Personal access tokens > Generate new token
8) git remote set-url origin https://ghp_y1gKcGkUeIMRgGoxp0Ztk_your_token_tS1@github.com/tomasfn87/learningGit.git
 > git remote set-url origin https://(-------------your----token------------)@(----------https-clone-URL---------)
 * change the remote repository URL for fetch and push operations

VI. Push local files to github.com repository
---------------------------------------------
9) git push -u origin main
 > git push origin main
 * push/send files to repository; option -u is required only the first time

VII. To fetch files that are on the github repository but not on your local folder
----------------------------------------------------------------------------------
10) git pull origin main --allow-unrelated-histories
 * sometimes you must pull files from github before pushing from local repository
 * --allow-unrelated-histories helps your merge local and git files

11) git checkout -b "new-button"
 * leaves actual branch and goes to the newly created "new-button" branch
 > git checkout "main"
 * leaves actual branch and goes to the existing "main" branch
 > git checkout "new-button"
 * leaves actual branch and foes to the existing "new-button" branch
 
12) git branch (--list) 
 * shows a list of branches; the actual branch will be green and marked with an asterisk (*)