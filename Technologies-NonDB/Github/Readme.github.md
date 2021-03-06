Github
======


* Most frequent used commands to add changes to server
```
git add *
git commit -m "Comment about the change"
git push
```
* Push changes to specific branch on server
    - `git push origin BranchName`
* How to clone a new Repo Example
```
git clone https://github.com/vijred/Powershell.git
git clone https://orgname@dev.azure.com/prgname/Project1/_git/Project1 c:\VJ\otherrepos\AzureDevops\Project1 --progress
```
* How to pull latest version 
```
git pull
```
* Hardreset
```
git fetch origin
git reset --hard origin/master
```
* Credential Management commands
```
Credential Management:
git remote
git remote set-url origin git@github.com:yourname/yourrepo.git
```
* Check status of changes
    - `Git status`
* Create local git repo - Convert a project as local repo
    - `git init`

* Find git remote server info
    - `git remote -v`
* Find the differences in last 2 comments
    - `git diff -2`
* Comment tree
```
git log --graph --decorate --pretty=oneline --abbrev-commit --all
git log --all --graph --pretty=format:'%C(yellow)%h%Creset%C(blue)%d%Creset %C(white bold)%s%Creset %C(white dim)(%an on %ai [%ar])%Creset'
```


Branch:
-------
* List all branches in local repo
    - `Git branch`
* Create new branch 
    - `git branch -b NewBranchname`
* Switch a branch
    - `git checkout BranchName`
* Delete a branch
    - `git branch -D DeletingBranchName`


Config
------
* How to edit gitconfig file
    -   `git config --global --edit` 
* Disable SSL Verify
    -   `git config --global http.sslVerify false`


Tips:
-----
* How to correct the mistakes while pushing the data -> https://about.gitlab.com/blog/2018/08/08/git-happens/ 
* Basic commands -> https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html 
* How to remove sensitive data from one of the files in github -> https://rtyley.github.io/bfg-repo-cleaner/ 
* Troubleshoot gitbug certificate issues - https://stackoverflow.com/questions/23885449/unable-to-resolve-unable-to-get-local-issuer-certificate-using-git-on-windows
