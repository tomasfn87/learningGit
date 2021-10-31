I. Create a new repository
--------------------------
1) git init
 * start new repository for the current folder (?)

 > git clone URL
 > git clone https://github.com/tomasfn87/learningGit.git
 * If you created your remote repository first, then you use "git clone" to download it and make changes locally.

II. Stage files - prepare files to be commited
----------------------------------------------
2) git add Readme.md
 * Add file(s) or folder(s) to be staged

 > git add -a -m "Commit message"
 * To add files that are already being tracked and were modified.

 > git add -A -m "Commit message"
 * To add all files on the repository, including new files and files already tracked that wer modified.

III. Commit files to local repository
-------------------------------------
3) git status
 * see staged files awaiting to be commited

4) git commit -m "first commit"
 * commit staged files with -m "message"

IV. Setup GitHub repository
---------------------------
5) git branch -M main_branch_name
 * Sets "main_branch_name" as the root, main or master branch
 * The standard name for "git" is "master" (when you use the "git init" command); the standard name when you create your repository at GitHub.com is "main"
 * You may use this to rename your branch from "master" to "main" in case it was created locally using "git init" instead of creating it directly at "GitHub.com" and using "git clone" to start the actual work.

6) git remote add origin git@github.com:userName/repositoryName.git
 > git remote add origin git@github.com:tomasfn87/learningGit.git
 * add the URL for the destination repository as alias "origin"

7) git remote -v
 * show remote URL for fetch/push operations;

V. Add authentication token
---------------------------
Get your token:
> github.com > Settings > Developer settings > Personal access tokens > Generate new token

* You have to select the right permissions for what you are going to do with the repository.
8) git remote set-url origin https://(-------------your----token-----------)@(--------------clone-URL--------------)

 > git remote set-url origin https://ghp_y1gKcGkUeIMRgGoxp0Ztk_your_token_tS@github.com/username/repository_name.git
 * Change the remote repository URL for fetch and push operations

VI. Push local files to github.com repository
---------------------------------------------
9) git push -u origin main
 > git push origin main
 * Push/send files to repository; option -u is required only the first time
 * Will prompt for username and password (password is view-safe on WSL 2, at least)

VII. To fetch files that exist only in the github repository to your local folder
---------------------------------------------------------------------------------
10) git pull origin main --allow-unrelated-histories
 * Sometimes you must pull files from github before pushing from local repository
 * --allow-unrelated-histories helps your merge local and git files when there are files on the remote repository that don't exist locally yet

IX. To create and switch to a new branch (and back); to merge branches
----------------------------------------------------------------------
11) git checkout -b "new-button"
 * Leaves actual branch and goes to the newly created branch named "new-button"

 > git branch "navbar"
 * Creates a new branch called "navbar"

 > git checkout "main"
 * Leaves actual branch and goes to the existing "main" branch

 > git checkout "new-button"
 * Leaves actual branch and goes to the existing "new-button" branch

12) git branch (--list) 
 * The "--list" argument is optional ("git branch" == "git branch --list")
 * Shows a list of branches; the actual branch will typically be green and marked with an asterisk (*)

13) (git branch) (git checkout "main") git merge new-button
 * While in main (check with git branch and switch branches with gut checkout "branch_name"), merge new-button's and main's files, that can then be uploaded to the repository with git add . && git commit -m "message"

14) > git restore file... 
   * Revert a file to an earlier version stored locally

   > git restore --staged file...
   * Remove a file from stage (it means it will no longer be commited now)

   > git rm --cached file...
   * To unstage files that are awaiting to be commited (added via git add)
   
   > git rm -f file...
   * To force removal of files that were staged and are awaiting to be commited
   
   > git revert 1a5b2f1 (commit)
   * Creates a new commit that registers that changes made on "1a5b2f1" were reverted, meaning this process can also be a undone.