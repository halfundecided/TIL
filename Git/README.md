# git commands -Mijeong Ban

## how to set up first? 
- Create a folder that I want to manage by using GitHub
- set README.md
- `git init` at that dir: initializes git repository
- `hub create`: link your git repository to GitHub
- `git add filename`
- `git commit -m "info about the changes you made"`
- `git push -u origin master` (only the first push needs this process) 
- create .gitignore file for all the files you do NOT want to track

## What did I need to do after changing GitHub username?
- in that dir, `git remote set-url origin https://github.com/halfundecided/reponame.git`
- `git remote -v`: verify new remote URL
- OR you can also use .git/config
- when you commits your new changes, if some fatal occurs -> `git push origin master`

## Basic commands 
- `git config --global --list`: see current config 
- `git --version`: check current version
- `git commit -C HEAD -a --amend`: change commit message by using the previous message`
- `git status`
- `git diff`: see difference btw stage and working tree
- `git diff --cached`: btw stage and repo
- `git diff HEAD`: btw repo, stage area and working tree
- `git checkout --filename`: cancel the changes and return the previous version
- `git clone url`: clone repo


## Branch & Tag
- `git branch`: check existing branch
- `git branch B A`: make new branch B from branch A
- `git branch A`: make new branch A
- `git branch -d A`: remove branch A
- `git branch -m existingBranch newBranch: change from existingBranch to newBranch
- 





## Linux lab
- `ssh linuxlab` : go to linuxlab  
- `scp filename linuxlab:~/` : copy file or folder into linux lab
- `make` : compile
- `/.filename` : test

## alias
- `vim .bashrc`: ~ 상태에서 `ls -a` 체크 한 뒤
- add nicknames 
- `source ~/.bashrc`
 
