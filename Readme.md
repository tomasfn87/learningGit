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
 * specify the branch to be pushed

6) git remote add origin git@github.com:userName/repositoryName.git
 - git remote add origin git@github.com:tomasfn87/learningGit.git
 * add the URL for the destination repository as alias "origin"

7) git remote -v
 * show remote URL for fetch/push operations; can be altered by step 8

V. Add authentication token
---------------------------
> github.com > Settings > Developer settings > Personal access tokens > Generate new token
8) git remote set-url origin https://ghp_y1gKcGkUeIMRgGoxp0Ztk_your_token_tS1@github.com/tomasfn87/learningGit.git
 - git remote set-url origin https://(-------------your----token------------)@(----------https-clone-URL---------)

VI. Push local files to github.com repository
---------------------------------------------
9) git push -u origin main
 - git push origin main
 * push/send files to repository; option -u is required only the first time

VII. To fetch files that are on the github repository but not on your local folder
----------------------------------------------------------------------------------
10) git pull origin main --allow-unrelated-histories
 * Sometimes you must pull files from origin before pushing from local repository
 * --allow-unrelated-histories helps your merge local and git files