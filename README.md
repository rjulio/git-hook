# How to enable git hooks

### Create a folder to store your hooks
  `mkdir ~/.myGitHooks`

### Copy files to created folder

### Give permision to execute to every file inside
  `sudo chmod +x ~/.mygitHooks/prepare-commit-msg`

### Config your git project core.hooksPath to your folder path
  `git config --global core.hooksPath /home/dev/.mygitHooks/`

### Give ir a try locally before pushing your commit

---

**OBS: Needs git version 2.35 or newer**
