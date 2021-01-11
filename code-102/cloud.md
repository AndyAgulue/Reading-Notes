# Version control and GIT
Version control systems are software that helps you track changes as you make your code. 
## Benefits of *Version Control*
```
- Creates workflows
- Work with all versions of commited files
- Makes sure that changes made to code don't conflict
- Keeps a history of all commited changes
```

*GIT* is the cmost commonly used version system and is becoming the standard for version control.

## Benefits of GIT
```
. Commits; Creates a snapshot of all your code at a poin in time.
. Branches; Let's each developer save changes in their own local repository (folder) and merge it to the 'main' branch.
. Simutaneous Development; Everyone has their own local copy of code and can work simulatneously on thier own branches.
```
### Files in Git are uploaded in *3* stages
**A** (git add) when you first modify a file, the changes only exist in your working directory, you add all the files that need to be tracked with git with the *git add* command.
**C** (git commit) Once you're happy with your file edits, commit them with the *git commit* command. **Always include a message describing what changed**.
**P** (git push origin main) send the code up from your local machine to the cloud/GitHub with the *git push origin command*.

### Git Commands
```
. git clone {url} = clone a repo from GitHub to your local machine
. git status = check if there are any red/untracked changes to your repository (green means it's being tracked!)
. git add . = add all the files that need to be tracked 
. git commit -m "enter message here" = add a caption/message to your commit/snapshot
. git push origin main = send the code up from your local machine to the cloud/GitHub
```
## GitHub
Is an cloud based platform that provides hosting for software development and version control using Git.

#### Terminology
Repositories: Developer lingo for folder
