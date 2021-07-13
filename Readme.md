1) git init
 - start new repository

2) git add Readme.md 
 - add files to be staged

3) git status 
 - see staged files awaiting to be commited

4) git commit -m "first commit" 
 - commit staged files with -m "message"

5) git branch -M main
 - specify the branch

6) git remote add origin git@github.com:userName/repositoryName.git
 - git remote add origin git@github.com:tomasfn87/learningGit.git
 - add repository

7) git remote -v

8) git remote set-url origin https://ghp_y1gKcGkUeIMRgGoxp0Ztk_your_token_tS1@github.com/tomasfn87/learningGit.git
 - git remote set-url origin https://(--------------your---token------------)@(-https-clone-URL------------------)

9) git push -u origin main
 - git push origin main
 - push/send files to repository; option -u is required only the first time

10) git pull origin master --allow-unrelated-histories 
 - Sometimes you must pull files from origin before pushing from local repository