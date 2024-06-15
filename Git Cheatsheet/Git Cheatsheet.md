# Git CheatSheet

Git adalah sistem kontrol versi yang memungkinkan Anda melacak perubahan pada file dan folder. Ini adalah alat canggih yang dapat digunakan untuk segala hal mulai dari proyek pribadi kecil hingga aplikasi perusahaan berskala besar.

Panduan ini adalah referensi singkat ke perintah Git yang paling umum. Ini tidak dimaksudkan sebagai panduan komprehensif tentang Git, melainkan referensi singkat ke perintah-perintah yang paling umum.

# Setup and Configuration

```
git init // Initialize a new Git repository

git clone <url> // Clone and create a local copy of a remote repository

git config --global <setting_name> <value> // Configure global Git settings

git config --local <setting_name> <value> // Configure local Git settings for a specific repo

# --------------- Advanced ------------------


git config --list // Show a summary of your Git configuration settings

git config --global core.editor "<editor_command>" // Set a custom text editor for Git messages

git config --global alias.<shortcut> <command> // Create a Git command alias

git config --global color.ui auto // Enable automatic colorization of Git output

git config --global credential.helper 'cache --timeout=<seconds>' // Cache Git credentials for a certain amount of time

git config --global core.whitespace <options> // Configure git to detect specific types of whitespace errors

git config --global fetch.prune true // Automatically prune remote-tracking branches when fetching updates

git config --global diff.tool <tool> // Set a custom diff tool for Git

git config --global merge.tool <tool> // Set a custom merge tool for Git

git difftool // Compare changes using a custom diff tool

git mergetool // Resolve merge conflicts with a custom merge tool
```

# File Operations

```
git status // Show working tree status

git add <file(s)> // Add files to the staging area

git rm <file(s)> // Remove files from working tree and staging area

git mv <old_file> <new_file> // Move or rename a file

git commit -m "commit message" // Commit changes with a message

git diff // Show differences between working tree and last commit

# --------------- Advanced ------------------


git update-index --assume-unchanged <file> // Assume a tracked file is unchanged

git update-index --no-assume-unchanged <file> // Restore normal behavior of tracking changes

git diff <commit_id1>..<commit_id2> // Show differences between two commits

git rm --cached <file_name> // Unstage a file, but keep in the working directory

```

# Branching and Merging

```
git branch // List all branches

git branch <branch_name> // Create a new branch

git checkout <branch_name> // Switch to a specific branch

git merge <branch_name> // Merge a branch into the current branch

git branch -d <branch_name> // Delete a specific branch

git branch -r // List all remote branches

# --------------- Advanced ------------------


git branch -vv // List branches with additional information

git checkout -b <branch_name> <remote_name>/<remote_branch> // Create a new branch based on a remote branch

git merge --abort // Cancel merge in case of conflicts

git rebase <branch_name> // Rebase the current branch onto another branch

git rebase --abort // Cancel an ongoing rebase operation

git rebase -i // Interactive rebase for edit, squash, re-order or drop commits

git rebase -i <remote_name>/<remote_branch> // Rebase commits in the current branch onto a remote branch interactively
```

# Remote Repositories

```
# List remote repositories
git remote
# Add a remote repository
git remote add <name> <url>
# Fetch from a remote repository
git fetch <remote_name>
# Pull changes from a remote branch
git pull <remote_name> <remote_branch>
# Push changes to a remote repository
git push <remote_name> <local_branch>
# Remove a remote repository
git remote rm <remote_name>
# Display information about a specific remote repository
git remote show <remote_name>
# Show the tracking branches for remote repositories
git remote show <remote_name> --verbose

# --------------- Advanced -------------------


git remote update // Fetch updates from all remote repositories

git push --force <remote_name> <local_branch> // Force-push changes to a remote repository, overwriting remote history

git push --tags <remote_name> // Push all tags to a remote repository

git remote rename <old_name> <new_name> // Rename a remote repository

git remote set-url <name> <new_url> // Change the URL of a remote repository

git remote prune <remote_name> // Remove stale remote-tracking branches

git branch -r --merged // List all remote branches that have been merged into the current branch

git branch -r --no-merged // List all remote branches not yet merged into the current branch

git fetch -p // Fetch updates from a remote repository and prune obsolete remote-tracking branches

git branch --track <branch_name> <remote_name>/<remote_branch> // Track a remote branch and set up the local branch to automatically sync with it

git branch -u <remote_name>/<remote_branch> // Set an existing local branch to track a remote branch

git push -u <remote_name> <local_branch> // Push a branch to a remote repository and set it to track the remote branch

git branch --unset-upstream <branch_name> // Remove the tracking association between a local and a remote branch
```

# Commit History

```
git log // Show commit history

git log --oneline // Display a condensed commit history

git log --graph // Show branching commit history

git log --author=<author_name> // Filter commit history by author

git log --since=<date> // Show commit history since specific date

git log --until=<date> // Show commit history until specific date
```

# Tags

```
git tag // List all tags

git tag <tag_name> <commit_id> // Create a new tag at a specific commit

git tag -a <tag_name> -m "tag message" // Create an annotated tag with a message

git tag -d <tag_name> // Delete a specific tag

git push <remote_name> --delete <tag_name> // Delete a specific remote tag

git show <tag_name> // Show information about a specific tag
```

# Stashes

```
git stash save "stash message" // Temporarily save changes in the working tree

git stash list // List all stashes

git stash apply <stash> // Apply changes from a specific stash

git stash drop <stash> // Remove a specific stash

git stash clear // Remove all stashes

```

# Cherry-Picking

```
git cherry-pick <commit_id> // Apply a specific commit from one branch to another
```

# Commit Management

```
git commit --amend // Modify the latest commit

git revert <commit_id> // Create a new commit that undoes changes from a previous commit

git reset --hard <commit_id> // Discard changes and move HEAD to a specific commit

git reset --soft <commit_id> // Move HEAD to a specific commit, but preserve staged changes

git reflog // Show a record of all changes made to the local repository head
```

# Submodules, Subtrees, and Advanced Submodules

```
git submodule add <repository_url> <path> // Add a submodule to the current repository

git submodule update --init --recursive // Initialize and update all submodules recursively

git subtree add --prefix=<path> <repository_url> // Add a subtree to the current repository

git submodule init // Initialize the submodules in the repository

git submodule update // Update the submodules to their latest commits

git submodule foreach <command> // Execute a specific command in each submodule

git submodule deinit <path> // Unregister a submodule
```

# Hooks and Automation, and Diff and Merge Tools

```
git hooks // Locate hooks directory in the Git repository (usually in .git/hooks/)

pre-commit, post-commit, pre-push, post-merge, etc. // Script names for specific hooks that can be added to the hooks directory

chmod +x <hook_script> // Make a hook script executable to ensure it's triggered when necessary
```

# Work with Patches

```
git format-patch <commit_id> // Generate a patch file for a specific commit

git apply <patch_file> // Apply a patch to the current branch

git am <patch_file> // Apply a patch using the "git am" (apply mailbox) command
```

# Collaboration

```
git request-pull <start_commit> <end_commit> <url> // Generate a request-pull summary with the changes between two commits

git shortlog // Summarize the commit history, listing authors and their contributions

git ls-files // List all files tracked by Git

git grep <pattern> // Search for a specified pattern in files tracked by Git
```

# Bisecting, Debugging, and Performance Issues

```
git bisect start // Begin a bisect session to find the commit that introduced a bug

git bisect bad <commit_id> // Mark a commit as "bad," indicating it contains the bug

git bisect good <commit_id> // Mark a commit as "good," indicating it does not contain the bug

git bisect reset // End the bisect session and return to the original branch/commit

git fsck // Verify the integrity of the Git repository

git gc // Run garbage collection to optimize the repository's performance

git clean -df // Remove untracked files and directories (use with caution)
```

# Tips and Tricks

```
git add -p // Interactively choose parts (hunks) of files to stage

git log -p <file_name> // Show the commit history and associated patches for a specific file


git log --pretty=format:"%h - %an, %ar : %s" // Customize the format of the git log output

git log --grep="<text>" // Find text in commit messages (useful for locating specific changes)

git diff --stat // Quickly view the changes in the working directory since the last commit

git log --oneline --decorate --graph // Display the branch history with decoration to see where branches have split or merged


git stash save -u // Stash changes in the working tree, including untracked files

git commit --allow-empty -m "Empty commit message" // Create an empty commit, useful while testing branch protection rules


git config --global core.pager 'less -RFX' // Set the git output pager to quit when the output is less than one screen, and not clear the screen after displaying

git config --global help.autocorrect 1 // Use Git's auto-correct feature to fix mistyped commands

git config --get-regexp alias // List aliases for Git commands


git merge --no-commit --no-ff <branch_name> // Perform a dry run of merging without actually merging branches

git ls-tree --name-only -r -t HEAD // Show a tree-like representation of the repo's structure
```
