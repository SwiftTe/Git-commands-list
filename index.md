
# Git Commands List

## 1. Initial Setup
These are the first commands you'll run when setting up Git and GitHub on your system.

### Set up global username
```bash
git config --global user.name "Your Name"
Set up global email

git config --global user.email "your_email@example.com"
View Git configurations
bash
Copy code
git config --list
Set default branch to main instead of master (optional)
bash
Copy code
git config --global init.defaultBranch main
2. Creating/Cloning a Repository
Start managing your project with Git.

Initialize a new Git repository
bash
Copy code
git init
Clone a remote repository
bash
Copy code
git clone <repository_url>
3. Staging and Committing Changes
To track changes in files and create a history.

Check the status of files
bash
Copy code
git status
Add specific file(s) to the staging area
bash
Copy code
git add <file_name>
Add all files to the staging area
bash
Copy code
git add .
Commit changes with a message
bash
Copy code
git commit -m "Your commit message"
Commit and stage all modified tracked files in one step
bash
Copy code
git commit -am "Your commit message"
4. Working with Branches
Creating, switching, and managing branches.

Create a new branch
bash
Copy code
git branch <branch_name>
Switch to a specific branch
bash
Copy code
git checkout <branch_name>
Create and switch to a new branch in one step
bash
Copy code
git checkout -b <branch_name>
List all branches
bash
Copy code
git branch
Merge a branch into the current branch
bash
Copy code
git merge <branch_name>
Delete a local branch
bash
Copy code
git branch -d <branch_name>
5. Pushing and Pulling Changes
Sync your local changes with a remote repository.

Add a remote repository
bash
Copy code
git remote add origin <repository_url>
Push changes to the remote repository
bash
Copy code
git push origin <branch_name>
Push changes when the upstream is already set
bash
Copy code
git push
Pull changes from the remote repository
bash
Copy code
git pull origin <branch_name>
Pull changes when the upstream is already set
bash
Copy code
git pull
6. Undoing Changes
Undo, reset, or fix changes when you make mistakes.

Unstage a file but keep the changes
bash
Copy code
git reset <file_name>
Discard changes in a file (working directory only)
bash
Copy code
git checkout -- <file_name>
Revert to a previous commit (keeps history)
bash
Copy code
git revert <commit_hash>
Reset to a previous commit (removes history)
bash
Copy code
git reset --hard <commit_hash>
Modify the last commit (amend)
bash
Copy code
git commit --amend
7. Git Logs and History
Explore commit history and changes.

View commit history
bash
Copy code
git log
View commit history in one line per commit
bash
Copy code
git log --oneline
Show changes between commits or the working directory
bash
Copy code
git diff
Show changes between current branch and another branch
bash
Copy code
git diff <branch_name>
8. Tagging (Versioning)
Tagging releases or important points in your history.

Create a new tag
bash
Copy code
git tag <tag_name>
Push a specific tag
bash
Copy code
git push origin <tag_name>
Push all tags
bash
Copy code
git push --tags
9. Collaboration Commands
Working with others on a project.

Create a pull request
Use GitHub's GUI or, if using the Hub CLI, you can run:

bash
Copy code
hub pull-request
Fork a repository
Fork using GitHub's interface, then:

bash
Copy code
git clone <forked_repo_url>
10. Stashing Changes
Temporarily saving uncommitted changes.

Stash changes
bash
Copy code
git stash
Apply the last stashed changes
bash
Copy code
git stash pop
List all stashes
bash
Copy code
git stash list
11. Rebasing and Squashing
Reorganize commits before merging or updating branches.

Rebase your branch onto another
bash
Copy code
git rebase <branch_name>
Squash commits into one (interactive rebase)
bash
Copy code
git rebase -i HEAD~n
12. GitHub Pages Deployment
Deploy your project to GitHub Pages.

Create a branch for GitHub Pages deployment (for non-main branch deployment)
bash
Copy code
git checkout -b gh-pages
Push the branch to GitHub Pages
bash
Copy code
git push origin gh-pages
On GitHub (via web GUI): Navigate to your repository → Settings → Pages → Select your branch (usually gh-pages) and set it as the source for GitHub Pages.

13. Managing Remotes
Handling remote repositories.

View all remote repositories
bash
Copy code
git remote -v
Change remote URL
bash
Copy code
git remote set-url origin <new_url>
Remove a remote
bash
Copy code
git remote remove origin
14. Deleting Repositories (Local and Remote)
Cleaning up repositories.

Remove the Git repository (keep files, remove .git folder)
bash
Copy code
rm -rf .git
Delete a remote repository
Done via the GitHub web interface (Settings → Danger Zone → Delete this repository).

Copy code
