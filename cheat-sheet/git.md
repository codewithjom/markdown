# :point_right: Git Cheat Sheet

### Table of Contents

- [Creating snapshots](#creating-snapshots)
    - [Initializing a repository](#initializing-repository)
    - [Staging files](#staging-files)
    - [Viewing the status](#viewing-status)
    - [Committing the staged files](#committing-stage-files)
    - [Skipping the staging area](#skipping-staging-area)
    - [Removing files](#removing-files)
    - [Viewing the staged/unstaged changes](#stage-unstage)
    - [Viewing the history](#viewing-history)
    - [Viewing a commit](#viewing-commit)
    - [Unstaging files (undoing git add)](#unstaging-files)
    - [Discarding local changes](#discard-local-changes)
    - [Restoring and earlier version of a file](#restoring-version)
- [Browsing history](#browsing-history)
    - [Viewing the history](#viewing-history2)
    - [Filtering the history](#filtering-history)
    - [Formatting the log output](#formatting-log-output)
    - [Creating an alias](#creating-alias)
    - [Viewing a commit](#viewing-commit)
    - [Comparing commits](#comparing-commits)
    - [Checking out a commit](#checking-out-commit)
    - [Finding a bad commit](#finding-a-bad-commit)
    - [Finding contributors](#finding-contributors)
    - [Viewing the history of a file](#viewing-history-of-a-file)
    - [Finding the author of lines](#finding-author)
- [Branching and Merging](#branching-and-merging)
    - [Managing branches](#managing-branches)
    - [Comparing branches](#comparing-branches)
    - [Stashing](#stashing)
    - [Merging](#merging)
    - [Viewing the merged branches](#viewing-merged-branches)
    - [Rebasing](#rebasing)
    - [Cherry picking](#cherry-picking)
- [Collaboration](#collaboration)
    - [Cloning a repository](#clone-repository)
    - [Syncing with remotes](#syncing-remotes)
    - [Sharing branches](#sharing-branches)
    - [Managing remotes](#managing-remotes)
- [Rewriting History](#rewriting-history)
    - [Undoing commits](#undoing-commits)
    - [Reverting commits](#reverting-commits)
    - [Recovering lost commits](#recovering-lost-commits)
    - [Amending the last commit](#amending-last-commit)
    - [Interactive rebasing](#interactive-rebasing)

## Creating snapshots <a id='creating-snapshots'></a>
### Initializing a repository <a id='initializing-repository'></a>

``` sh
git init
```

### Staging files <a id='staging-files'></a>

``` sh
git add file1.txt            # Stages a single file
git add file1.txt file2.txt  # Stages a multiple files
git add *.txt                # Stages with a pattern
git add .                    # Stages the current directory and all its content
```

### Viewing the status <a id='viewing-status'></a>

``` sh
git status     # Full status
git status -s  # Short status
```

### Committing the staged files <a id='committing-stage-files'></a>

``` sh
git commit -m "Message"  # Commits wiht one-line message
git commit               # Opens the default editory to type a long message
```

### Skipping the staging area <a id='skipping-staging-area'></a>

``` sh
git commit -am "Message"
```

### Removing files <a id='removing-files'></a>

``` sh
git rm file1.txt           # Removes from working directory and staging area
git rm --cached file1.txt  # Removes from staging area only
```

### Viewing the staged/unstaged changes <a id='stage-unstage'></a>

``` sh
git diff           # Shows unstaged changes
git diff --staged  # Shows staged changes
git diff --cached  # Same as the above
```

### Viewing the history <a id='viewing-history'></a>

``` sh
git log            # Full history
git log --oneline  # Summary
git log --reverse  # Lists the commits from the oldest to the newest
```

### Viewing a commit <a id='viewing-commit'></a>

``` sh
git show 921a2ff        # Shows the given commit
git show HEAD           # Shows the last commit
git show HEAD~2         # Two steps before the last commit
git show HEAD:file.txt  # Shows the version of the file.txt stored in the last commit
```

### Unstaging files (undoing git add) <a id='unstaging-files'></a>

``` sh
git restore --staged file.txt    # Copies the last version of file.txt from repo to index
```

### Discarding local changes <a id='discard-local-changes'></a>

``` sh
git restore file.txt              # Copies file.txt from index to working directory
git restore file1.txt file2.txt   # Restores multiple files in working directory
git restore .                     # Discards all local changes (except untracked files)
git cleam -fd                     # Removes all untracked files
```

### Restoring an earlier version of a files <a id='restoring-version'></a>

``` sh
git restore --source=HEAD~2 file.txt
```

## Browsing history
### Viewing the history <a id='viewing-history2'></a>

``` sh
git log --stat         # Shows the list of modified files
git log --patch        # Shows the actual changes (patches)
```

### Filtering the history <a id='filtering-history'></a>

``` sh
git log -3                      # Shows the last 3 entries
git log --author="Jom"
git log --before="2022-02-22"
git log --after="one week ago"
git log --grep="GUI"            # Commits with "GUI" in their message
git log -S"GUI"                 # Commits with "GUI" in their patches
git log hash1..hash2            # Range of commits
git log file.txt                # Commits that touched file.txt
```

### Formatting the log output <a id='formatting-log-output'></a>

``` sh
git log --pretty=format:"%an commited %H"
```

### Creating an alias <a id='creating-alias'></a>

``` sh
git config --global alias.lg "log --oneline"
```

### Viewing a commit <a id='viewing-commit'></a>

``` sh
git show HEAD~2
git show HEAD~2:file1.txt   # Shows the version of file stored in this commit
```

### Comparing commits <a id='comparing-commits'></a>

``` sh
git diff HEAD~2 HEAD           # Shows the changes between two commits
git diff HEAD~2 HEAD file.txt  # Changes to file.txt only
```

### Checking out a commit <a id='checking-out-commit'></a>

``` sh
git checkout dad47ed  # Checks out the given commit
git checkout master   # Checks out the master branch
```

### Finding a bad commit <a id='finding-a-bad-commit'></a>

``` sh
git bisect start
git bisect bad          # Marks the current commit as bad commit
git bisect good ca49180 # Marks the given commit as a good commit
git bisect reset        # Terminates the bisect session
```

### Finding contributors <a id='finding-contributors'></a>

``` sh
git shortlog
```

### Viewing the history of a file <a id='viewing-history-of-a-file'></a>

``` sh
git log file.txt          # Shows the commits that touched file.txt
git log --stat file.txt   # Shows statistics (the number of changes) for file.txt
git log --patch file.txt  # Shows the patches (changes) applied to file.txt
```

### Finding the author of lines <a id='finding-author'></a>

``` sh
git blame file.txt     # Shows the author of each line in file.txt
```

## Branching and Merging <a id='branching-and-merging'></a>
### Managing branches <a id='managing-branches'></a>

``` sh
git branch bugfix     # Creates a new branch called bugfix
git checkout bugfix   # Swithes to the bugfix branch
git switch bugfix     # Same as the above
git switch -C bugfix  # Creates and swithes
git branch -d bugfix  # Deletes the bugfix branch
```

### Comparing branches <a id='comparing-branches'></a>

``` sh
git log master..bugfix    # Lists the commits in the bugfix branch not in master
git diff master..bugfix   # Shows the summary of changes
```

### Stashing <a id='stashing'></a>

``` sh
git stash push -m "New tax rules."  # Creates a new stash
git stash list                      # Lists all the stashes
git stash show stash@{1}            # Shows the given stash
git stash show 1                    # Shortcut for stash@{1}
git stash apply 1                   # Applies the given stash to the working dir
git stash drop 1                    # Deletes the given stash
git stash clear                     # Deletes all the stashes
```

### Merging <a id='merging'></a>

``` sh
git merge bugfix               # Merges the bugfix branch into the current branch
git merge --no-ff bugfix       # Creates a merge commit even if FF is possible
git merge --squash bugfix      # Performs a squash merge
git merge --abort              # Aborts the merge
```

### Viewing the merged branches <a id='viewing-merged-branches'></a>

``` sh
git branch --merged      # Shows the merged branches
git branch --no-merged   # Shows the unmerged branches
```

### Rebasing <a id='rebasing'></a>

``` sh
git rebase master     # Changes the base of the current branch
```

### Cherry picking <a id='cherry-picking'></a>

``` sh
git cherry-pick dad47ed  # Applies the given commit on the current branch
```

## Collaboration <a id='collaboration'></a>
### Cloning a repository <a id='clone-repository'></a>

``` sh
git clone url
```

### Syncing with remotes <a id='syncing-remotes'></a>

``` sh
git fetch origin master     # Fetches master from origin
git fetch origin            # Fetches all objects from origin
git fetch                   # Shortcut for "git fetch origin"
git pull                    # Fetch + merge
git push origin master      # Pushes master to origin
git push                    # Shortcut for "git push origin master"
```

### Sharing branches <a id='sharing-branches'></a>

``` sh
git branch -r              # Shows remote tracking branches
git branch -vv             # Shows local & remote tracking branches
git -u origin bugfix       # Pushes bugfix to origin
git push -d origin bugfix  # Removes bugfix from origin
```

### Managing remotes <a id='managing-remotes'></a>

``` sh
git remote                    # Shows remote repos
git remote add upstream url   # Adds a new remote called upstream
git remote rm upstream        # Remotes upstream
```

## Rewriting History <a id='rewriting-history'></a>
### Undoing commits <a id='undoing-commits'></a>

``` sh
git reset --soft HEAD^   # Removes the last commit, keeps changed staged
git reset --mixed HEAD^  # Unstages the changes as well
git reset --hard HEAD^   # Discards local changes
```

### Reverting commits <a id='reverting-commits'></a>

``` sh
git revert 72856ea    # Reverts the given commit
git rever HEAD~3..    # Reverts the last three commits
git rever --no-commit HEAD~3..
```

### Recovering lost commits <a id='recovering-lost-commits'></a>

``` sh
git reflog               # Shows the history of HEAD
git reflog show bugfix   # Shows the history of bugfix pointer
```

### Amending the last commit <a id='amending-last-commit'></a>

``` sh
git commit --amend
```

### Interactive rebasing <a id='interactive-rebasing'></a>

``` sh
git rebase -i HEAD~5
```
