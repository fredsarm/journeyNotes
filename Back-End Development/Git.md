# Most Commonly Used Git Commands
by ChatGPT

Here’s a guide with the most commonly used Git commands, along with brief explanations for each:

### 1. **Initialize a repository**
```bash
git init
```
Creates a new Git repository in the current directory. This is the first step to start version controlling your project.

---

### 2. **Add files to the stage (prepare for commit)**
```bash
git add <file>
```
Adds specific files or changes to the stage (staging area). To add all changed files, use:
```bash
git add .
```

---

### 3. **Check the status of the repository**
```bash
git status
```
Displays the status of files in the repository, showing which files have been modified, staged, or are untracked.

---

### 4. **Commit changes**
```bash
git commit -m "Commit message"
```
Saves the changes in the repository with a descriptive message. It’s good practice to commit frequently with clear messages about what was changed.

---

### 5. **Check the commit history**
```bash
git log
```
Shows the commit history of the repository, including details like the author, date, and commit message.

---

### 6. **Create and switch to a new branch**
```bash
git checkout -b <branch-name>
```
Creates a new branch and switches to it at the same time. Branches are used to work on different features in isolation.

---

### 7. **Switch to an existing branch**
```bash
git checkout <branch-name>
```
Switches to an existing branch in the repository.

---

### 8. **Merge a branch**
```bash
git merge <branch-name>
```
Merges the changes from one branch into the current branch. Make sure you are on the branch that will receive the changes before merging.

---

### 9. **Clone a repository**
```bash
git clone <repository-url>
```
Clones a remote repository (like from GitHub) to your local directory.

---

### 10. **List branches**
```bash
git branch
```
Displays the list of branches in the repository. The current active branch will have an asterisk (*) next to its name.

---

### 11. **Push changes to a remote repository**
```bash
git push origin <branch-name>
```
Pushes the commits from the local branch to the remote repository (e.g., GitHub). For the first push of a branch, use:
```bash
git push -u origin <branch-name>
```

---

### 12. **Pull changes from the remote repository**
```bash
git pull
```
Downloads the latest changes from the remote repository to your local directory and merges them automatically.

---

### 13. **Discard changes in a file**
```bash
git checkout -- <file>
```
Discards the changes made to a file that hasn’t been committed, restoring it to the last commit state.

---

### 14. **Revert a commit**
```bash
git revert <commit-hash>
```
Creates a new commit that undoes the changes of the specified commit. This preserves the commit history.

---

### 15. **Rebase a branch**
```bash
git rebase <branch-name>
```
Moves or reapplies commits from your current branch onto another branch, maintaining a linear history without merge commits.

---

### 16. **Show differences between commits**
```bash
git diff
```
Shows the differences between modified, staged, and committed files.

---

### 17. **Delete a branch**
```bash
git branch -d <branch-name>
```
Deletes a local branch. The `-d` flag only works if the branch has been merged. Use `-D` to force delete.