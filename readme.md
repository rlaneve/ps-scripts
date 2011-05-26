# PowerShell Scripts

## Git

### git-aliases.ps1
Many of these are just command shorteners, 'cause I'm that lazy.

#### gs
Runs 'git status'

#### glog
Runs 'git log' with a specific "pretty-format".

#### gbshare [branch_name]
Pushes specified branch to remote origin, sets up local branch to track remote and checks out local branch.

#### gbtrack [branch_name]
Creates new local branch setup to track remote branch and checks out new local branch.

#### gbdelete [branch_name]
Deletes specified branch from remote and local. Will *not* delete branches named "master" or "develop".

#### gco [branch_name]
Checks out specified branch.

#### gundo
Runs 'git reset --soft HEAD^1'. This reverses the last commit, leaving any changes to the working tree intact.

#### gca
Runs 'git add -A' followed by 'git commit'. Any supplied arguements will be passed to git commit.
This effectively stages all new files, modified files and removed files, and then commits.

#### gcam [commit_msg]
Runs 'git add -A' followed by 'git commit -m commit_msg'.
This effectively stages all new files, modified files and removed files, and then commits with the supplied message.

### git-reup.ps1
* stash any local changes
* pull latest from origin, rebasing local commits
* re-apply any stashed changes
* if new commits were pulled, display diffstat and log only for the new changes.
