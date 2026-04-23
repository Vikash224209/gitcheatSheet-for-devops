# Git Commands Reference

## 1. Initialization

- **Create a new Git repository:**

  ```
  git init
  ```

- **Clone an existing repository:**

  ```
  git clone <repository-url>
  ```

---

## 2. Configuration

- **Set global username:**

  ```
  git config --global user.name "YourName"
  ```

- **Set global email:**

  ```
  git config --global user.email "youremail@gmail.com"
  ```

- **Check current configuration:**

  ```
  git config --list
  ```

- **Set default branch name:**

  ```
  git config --global init.defaultBranch main
  ```

---

## 3. File Operations

- **Create a new file:**

  ```
  touch <filename>
  ```

- **Remove a file:**

  ```
  rm <filename>
  ```

- **Restore a deleted file:**

  ```
  git restore <filename>
  ```

- **Move or rename a file:**

  ```
  git mv <old-filename> <new-filename>
  ```

---

## 4. Staging & Committing

- **Check the status of your working directory:**

  ```
  git status
  ```

- **Stage a specific file:**

  ```
  git add <filename>
  ```

- **Stage all changes:**

  ```
  git add .
  ```

- **Unstage a file:**

  ```
  git restore --staged <filename>
  ```

- **Commit staged changes:**

  ```
  git commit -m "your commit message"
  ```

- **Stage and commit in one step:**

  ```
  git commit -am "your commit message"
  ```

- **Amend the last commit:**

  ```
  git commit --amend -m "updated commit message"
  ```

---

## 5. Viewing History

- **View commit history:**

  ```
  git log
  ```

- **View compact commit history:**

  ```
  git log --oneline
  ```

- **View history with graph:**

  ```
  git log --oneline --graph --all
  ```

- **Show changes in a specific commit:**

  ```
  git show <commit-hash>
  ```

- **View unstaged changes:**

  ```
  git diff
  ```

- **View staged changes:**

  ```
  git diff --staged
  ```

---

## 6. Branching

- **List all branches:**

  ```
  git branch
  ```

- **Create a new branch:**

  ```
  git branch <branch-name>
  ```

- **Switch to a branch:**

  ```
  git checkout <branch-name>
  ```

- **Create and switch to a new branch:**

  ```
  git checkout -b <branch-name>
  ```

- **Rename a branch:**

  ```
  git branch -m <old-name> <new-name>
  ```

- **Delete a branch (local):**

  ```
  git branch -d <branch-name>
  ```

- **Force delete a branch:**

  ```
  git branch -D <branch-name>
  ```

---

## 7. Merging & Rebasing

- **Merge a branch into current branch:**

  ```
  git merge <branch-name>
  ```

- **Rebase current branch onto another:**

  ```
  git rebase <branch-name>
  ```

- **Abort a merge in progress:**

  ```
  git merge --abort
  ```

- **Abort a rebase in progress:**

  ```
  git rebase --abort
  ```

---

## 8. Stashing

- **Stash current changes:**

  ```
  git stash
  ```

- **List all stashes:**

  ```
  git stash list
  ```

- **Apply the latest stash:**

  ```
  git stash pop
  ```

- **Apply a specific stash:**

  ```
  git stash apply stash@{n}
  ```

- **Drop a specific stash:**

  ```
  git stash drop stash@{n}
  ```

- **Clear all stashes:**

  ```
  git stash clear
  ```

---

## 9. Remote Repositories

- **View remote connections:**

  ```
  git remote -v
  ```

- **Add a remote:**

  ```
  git remote add origin <repository-url>
  ```

- **Remove a remote:**

  ```
  git remote remove origin
  ```

- **Rename a remote:**

  ```
  git remote rename origin upstream
  ```

---

## 10. Pushing & Pulling

- **Push to remote branch:**

  ```
  git push origin <branch-name>
  ```

- **Push and set upstream tracking:**

  ```
  git push -u origin <branch-name>
  ```

- **Pull latest changes from remote:**

  ```
  git pull origin <branch-name>
  ```

- **Fetch changes without merging:**

  ```
  git fetch origin
  ```

- **Force push (use with caution):**

  ```
  git push --force origin <branch-name>
  ```

- **Delete a remote branch:**

  ```
  git push origin --delete <branch-name>
  ```

---

## 11. Undoing Changes

- **Discard changes in working directory:**

  ```
  git restore <filename>
  ```

- **Revert a specific commit (safe):**

  ```
  git revert <commit-hash>
  ```

- **Reset to a previous commit (soft — keeps changes staged):**

  ```
  git reset --soft <commit-hash>
  ```

- **Reset to a previous commit (mixed — unstages changes):**

  ```
  git reset --mixed <commit-hash>
  ```

- **Reset to a previous commit (hard — discards all changes):**

  ```
  git reset --hard <commit-hash>
  ```

---

## 12. Tags

- **Create a lightweight tag:**

  ```
  git tag <tag-name>
  ```

- **Create an annotated tag:**

  ```
  git tag -a <tag-name> -m "tag message"
  ```

- **List all tags:**

  ```
  git tag
  ```

- **Push a tag to remote:**

  ```
  git push origin <tag-name>
  ```

- **Push all tags to remote:**

  ```
  git push --tags
  ```

- **Delete a local tag:**

  ```
  git tag -d <tag-name>
  ```

---

## 13. Cherry Picking

- **Apply a specific commit to the current branch:**

  ```
  git cherry-pick <commit-hash>
  ```

---

## 14. Bisect (Debugging)

- **Start bisect session:**

  ```
  git bisect start
  ```

- **Mark current commit as bad:**

  ```
  git bisect bad
  ```

- **Mark a known good commit:**

  ```
  git bisect good <commit-hash>
  ```

- **End bisect session:**

  ```
  git bisect reset
  ```

---

## 15. Submodules

- **Add a submodule:**

  ```
  git submodule add <repository-url>
  ```

- **Initialize submodules:**

  ```
  git submodule init
  ```

- **Update submodules:**

  ```
  git submodule update
  ```

---

## 16. Aliases (Shortcuts)

- **Create an alias for a command:**

  ```
  git config --global alias.st status
  ```

- **Example — short log alias:**

  ```
  git config --global alias.lg "log --oneline --graph --all"
  ```

---

## 17. Cleanup

- **Remove untracked files (dry run first):**

  ```
  git clean -n
  ```

- **Remove untracked files:**

  ```
  git clean -f
  ```

- **Remove untracked files and directories:**

  ```
  git clean -fd
  ```
