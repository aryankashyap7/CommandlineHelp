# Git And Github Quick Command

This page contains all the most useful commands for git commandline interface.

---

### Changing Directory

| Command                | Description                   |
| ---------------------- | ----------------------------- |
| `cd </file/path/code>` | change directory to a project |

### Setting up user.name and user.email

| Command                                                     | Description                                 |
| ----------------------------------------------------------- | ------------------------------------------- |
| `git config --global user.name "Your Name"`                 | Assigns a global git username               |
| `git config --global user.email "youremail@yourdomain.com"` | Assigns a global git email                  |
| `git config --list`                                         | Lists the current global username and email |

### Getting & Creating Projects

| Command                                                           | Description                                |
| ----------------------------------------------------------------- | ------------------------------------------ |
| `git init`                                                        | Initialize a local Git repository          |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command                            | Description                                       |
| ---------------------------------- | ------------------------------------------------- |
| `git status`                       | Check status                                      |
| `git add [file-name.txt]`          | Add a file to the staging area                    |
| `git add .`                        | Add all new and changed files to the staging area |
| `git restore --staged <file>`      | Remove a file from staging area                   |
| `git commit -m "[commit message]"` | Commit changes                                    |
| `git rm -r [file-name.txt]`        | Remove a file (or folder)                         |

### Branching & Merging

| Command                                              | Description                                             |
| ---------------------------------------------------- | ------------------------------------------------------- |
| `git branch`                                         | List branches (the asterisk denotes the current branch) |
| `git branch -a`                                      | List all branches (local and remote)                    |
| `git branch [branch name]`                           | Create a new branch                                     |
| `git branch -d [branch name]`                        | Delete a branch                                         |
| `git push origin --delete [branch name]`             | Delete a remote branch                                  |
| `git checkout -b [branch name]`                      | Create a new branch and switch to it                    |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it                  |
| `git branch -m [old branch name] [new branch name]`  | Rename a local branch                                   |
| `git checkout [branch name]`                         | Switch to a branch                                      |
| `git checkout -`                                     | Switch to the branch last checked out                   |
| `git checkout -- [file-name.txt]`                    | Discard changes to a file                               |
| `git merge [branch name]`                            | Merge a branch into the active branch                   |
| `git merge [source branch] [target branch]`          | Merge a branch into a target branch                     |
| `git stash`                                          | Stash changes in a dirty working directory              |
| `git stash clear`                                    | Remove all stashed entries                              |

### Sharing & Updating Projects

| Command                                                                           | Description                                                 |
| --------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| `git push origin [branch name]`                                                   | Push a branch to your remote repository                     |
| `git push -u origin [branch name]`                                                | Push changes to remote repository (and remember the branch) |
| `git push`                                                                        | Push changes to remote repository (remembered branch)       |
| `git push origin --delete [branch name]`                                          | Delete a remote branch                                      |
| `git pull`                                                                        | Update local repository to the newest commit                |
| `git pull origin [branch name]`                                                   | Pull changes from remote repository                         |
| `git reset [commit id]`                                                           | Delete all commits after the provided commit id             |
| `git reset --hard [commit]`                                                       | To remove changes from working directory as well            |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git`     | Add a remote repository                                     |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH                     |
| `git cherry-pick [deleted commit id]`                                             | Restore all deleted commits before this commit              |

### Inspection & Comparison

| Command                                    | Description                    |
| ------------------------------------------ | ------------------------------ |
| `git log`                                  | View changes                   |
| `git log --summary`                        | View changes (detailed)        |
| `git log --oneline`                        | View changes (briefly)         |
| `git diff [source branch] [target branch]` | Preview changes before merging |

### Sync Github Repository

| Command                                           | Description                                 |
| ------------------------------------------------- | ------------------------------------------- |
| `git remote -v`                                   | Shows the current push and fetch repository |
| `git remote add origin [https link of main repo]` | Add main repo as upstream                   |
| `git fetch upstream`                              | Fetch all changes from main repo            |
| `git merge upstream/[branch-name]`                | Merge those changes to local repository     |
