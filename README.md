# git_commands
git commands referenced by atlassian-git-cheatsheet


## git Basics
- `git init <dir>` : Create empty git repo in specified directory. Run with no arguments to initialize the current directory.
- `git clone <dir>` : Clone repo located at *repo* onto local machine.
- `git add <dir>` : Stage all changes in *dir* for the next commit.
- `git commit -m "message"` : Commit the staged snapshot, but instead of launching a text editor, use *message* as the commit message.
- `git status` : List which files are staged, unstaged, and untracked.

## git Branches
- `git branch` : List all of the branches in your repo. Add a *branch* argument to create a new branch with the name *branch*.
- `git checkout -b <branch>` : Create and check out a new branch named *branch*. Drop the **-b** flag to checkout an existing branch.
- `git merge <branch>` : Merge *branch* into the current branch.

## Remote Repositories
- `git remote add <name> <url>` : Create a new connection to a remote repo. After adding a remote, you can use *name* as a shortcut for *url* in other commands.
- `git fetch <remote> <branch>` : Fetches a specific *branch*, from the repo. Leave off *branch* to fetch all remote refs.
- `git pull <remote>` : Fetch the specified remote's copy of current branch and immediately merge it into the local copy.
- `git pull --rebase <remote>` : Fetch the specified remote's copy of current branch and rebases it into the local copy. Uses git rebase instead of merge integrate the branches.
- `git push <remote> <branch> ` : Push the branch to *remote*, along with necessary commits and objects. Creates named branch in the remote repo if it doesn't exist.
- `git push <remote> --force` : Forces the `git push` even if it results in a non-fast-forward merge. Do not use the **--force** flag unless you're absolutely sure you know what you're doing.
- `git push <remote> --all` : Push all of your local branches to the specified remote.
- `git push <remote> --tags` : Tags aren't automatically pushed when you push a branch or use the **--all** flag. The **--tags** flag sends all of your local tags to the remote repo.

## git config
- `git config --global user.name <name>` : Define the author name to be used for all commits by the current user.
- `git config --global user.email <email>` : Define the author email to be used for all commits by the current user.
- `git config --global --edit` : Open the global configuration file in a text editor for manual editing.

## git log
- `git log -<limit>` : Limit number of commits by *limit*. E.g `git log -5` will limit to 5 commits.
- `git log --oneline` : Condense each commit to a single line.
- `git log -p` : Display the full diff of each commit.
- `git log --author="<pattern>"` : Search for commits by a particular author.
- `git log --grep="<pattern>"` : Search for commits with a commit message that matches *pattern*.
- `git log <since>..<until>` : Show commits that occur between *since* and *until*. Args can be commit ID, branch name, **HEAD**, or any other kind of revision reference.
- `git log --graph --decorate` : **--graph** flag draws a text based graph of commits on left side of commit msgs. **--decorate** adds names of branches or tags of commits shown.
