# How to enable git hooks

### Create a folder to store your hooks
  `mkdir ~/.myGitHooks`

### Copy files to created folder

### Give permision to execute to every file inside
  `sudo chmod +x ~/.mygitHooks/prepare-commit-msg`

### Config your git project core.hooksPath to your folder path
  `git config --global core.hooksPath /home/dev/.mygitHooks/`

### Give ir a try locally before pushing your commit

**OBS: Needs git version 2.35 or newer**


---


# Alias to improve productivity

`git for-each-ref refs/heads/ --format='%(color:yellow)%(refname:short)%(color:reset) - %(contents:subject) (%(color:green)%(committerdate:relative)%(color:reset))'`
Shows local branches + last commit + last branch  update

### BASH FUNCTIONS TO USE WITH GIT

Shows git log in a pretty format ($1 = number of logs to show)
```
gitLogFunction(){
	git log --graph --pretty=format:"%Cred%h%Creset | %C(yellow)%ad%Creset | %s | %C(bold blue)<%an>%Creset" -$1 --date=format:'%d/%m'
}
``` 

Show colored git diff
```
gitDiff(){
	git diff --color-words HEAD
}
```

Get all branches with given string in its name ($1 = any string)
```
showBulkBranches(){
	git branch | grep $1
}
```

Deletes all branches with given string in its name
```
deleteBulkBranches(){
	git branch | grep $1 | xargs git branch -D
}
```

Adds all items, created a commit with given msg and push
```
gitCP(){
	git add . && git commit -am "$1" && git push
}
```





