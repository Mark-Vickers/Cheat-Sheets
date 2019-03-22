# Basic Git Usage

## Setting up Git

### Configuring name and email address for commits
```bash
git config --global user.name "User Name"
git config --global user.email "email.address@example.com"
```

## Initialising local repository
```bash
git init
git add .
git commit -m "Initial commit"
```

## Looking at the repository
```bash
git status # status of current branch
git show # by default shows the last commit
git log --oneline --graph --decorate --all
git diff <filename> # shows diff since last commit
```
## Aliasing more complex commands
```bash
git config --global alias.hist "log --oneline --graph --decorate --all"
git hist
git config --global --unset alias.hist # to delete
```

## Pushing a local repository to GitHub
First create an empty repository on GitHub ready to receive the local files.
Make a note of the remote repository name.
```bash
git remote add origin <remote repository url>
git remote -v
git push -u origin master --tags # only on initial push
```

## Pushing changes to an existing repository
First check we are up to date.
`git fetch`
If we need to merge in changes then
'git pull`

```bash
git push # pushes current branch commits
```

## Branching
```bash
git checkout -b <name-of-branch> # creates new branch locally
git push -u origin <name-of-branch> # pushes new branch to remote
git push # works from now on to push current branch
```
Note: The -u flag is used for the initial push to set up tracking relationships.

## Merging
```bash
git checkout master
git merge <branch to merge>
```

## Deleting an unused branch
```bash
git checkout master
git branch --merged # check that branch to delete has been merged
git branch -d <branch-to-delete-locally>
git push origin :<branch-to-delete-on-github>
```

## Keeping up to date with GitHub
```bash
git fetch
git pull  # recommended
git fetch -p # prunes stale references i.e. deleted branches on github itself
git pull --all # synchronise all branches
```

