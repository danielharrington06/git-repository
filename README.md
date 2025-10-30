# Git Instructions
## Create a Repository that is Synced to a Local Folder
- On GitHub, create a repository with no `README.md`
- Click on 'Create' and copy the web URL or password-protected SSH key 
- Navigate to the folder on local PC
- In a Git Bash, terminal run the following:
```git
git init
git remote add origin {link to repo}
git add .
git commit -m "Initial commit"
git push -u origin main
```
- Now, a README.md can be created

## Remove Git Tracking from a Directory
Navigate to the directory in a Git Bash terminal and run the following:
```git
rm -rf .git
```

## Commit and Push Changes
```git
git add .
git commit -m "Message here"
git push
```

## Pull Changes
```git
git pull
```

## Fork a Repository
- Navigate to the repository to be forked
- Go to the forked version of this and copy the web URL or password-protected SSH key 
- In a Git Bash terminal, run the following:
```git
git clone {link to repository}
cd {repository-name}
```

## Merge a Repository
- In a Git Bash terminal, run the following:
```git
git remote add upstream {link to original repository}
git fetch upstream
git push upstream main:fork-main
```
- Then, go to the original repository on GitHub and approve the Pull Request
- Merge fork-main to main
- Delete fork-main

## Create a New Branch
- To create a new branch:
```git
git branch <branch-name>
git switch -c <branch-name>
git status #(check that * is next to <branch-name>
```

## Push from a New Branch
```git
git push -u origin <branch-name>
# from now on git push can be used
```

## Merge back to main
- Go on GitHub
- There should be an option to pull request
- Merge the branches, resolving conflicts if necessary
- The old branch can now be deleted safely

## Set Default Branch to Default to `main`
```git
git config --global init.defaultBranch main
```
