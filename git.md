# GIT

## CLRF --> LF after `git add .`
- If you already have checked out the code, the files are already indexed. After changing your git settings, say by running:
`git config --global core.autocrlf input `
- you should refresh the indexes with
`git rm --cached -r . `
- and re-write git index with
`git reset --hard`
