1. Initial Setup
These are the first commands you'll run when setting up Git and GitHub on your system.

Set up global username


git config --global user.name "Your Name"
Set up global email


git config --global user.email "your_email@example.com"
View Git configurations


git config --list
Set default branch to main instead of master (optional)


git config --global init.defaultBranch main


2. Creating/Cloning a Repository
Start managing your project with Git.

Initialize a new Git repository


git init
Clone a remote repository


git clone <repository_url>


3. Staging and Committing Changes
To track changes in files and create a history.

Check the status of files


git status
Add specific file(s) to the staging area


git add <file_name>
Add all files to the staging area


git add .
Commit changes with a message


git commit -m "Your commit message"
Commit and stage all modified tracked files in one step


git commit -am "Your commit message"


4. Working with Branches
Creating, switching, and managing branches.

Create a new branch


git branch <branch_name>
Switch to a specific branch


git checkout <branch_name>
Create and switch to a new branch in one step


git checkout -b <branch_name>
List all branches


git branch
Merge a branch into the current branch


git merge <branch_name>
Delete a local branch


git branch -d <branch_name>


5. Pushing and Pulling Changes
Sync your local changes with a remote repository.

Add a remote repository


git remote add origin <repository_url>
Push changes to the remote repository


git push origin <branch_name>
Push changes when the upstream is already set


git push
Pull changes from the remote repository


git pull origin <branch_name>
Pull changes when the upstream is already set


git pull


6. Undoing Changes
Undo, reset, or fix changes when you make mistakes.

Unstage a file but keep the changes


git reset <file_name>
Discard changes in a file (working directory only)


git checkout -- <file_name>
Revert to a previous commit (keeps history)


git revert <commit_hash>
Reset to a previous commit (removes history)


git reset --hard <commit_hash>
Modify the last commit (amend)


git commit --amend


7. Git Logs and History
Explore commit history and changes.

View commit history


git log
View commit history in one line per commit


git log --oneline
Show changes between commits or the working directory


git diff
Show changes between current branch and another branch


git diff <branch_name>


8. Tagging (Versioning)
Tagging releases or important points in your history.

Create a new tag


git tag <tag_name>
Push a specific tag


git push origin <tag_name>
Push all tags


git push --tags


9. Collaboration Commands
Working with others on a project.

Create a pull request
Use GitHub's GUI or, if using the Hub CLI, you can run:


hub pull-request
Fork a repository
Fork using GitHub's interface, then:


git clone <forked_repo_url>
10. Stashing Changes
Temporarily saving uncommitted changes.

Stash changes


git stash
Apply the last stashed changes


git stash pop
List all stashes


git stash list


11. Rebasing and Squashing
Reorganize commits before merging or updating branches.

Rebase your branch onto another


git rebase <branch_name>
Squash commits into one (interactive rebase)


git rebase -i HEAD~n


12. GitHub Pages Deployment
Deploy your project to GitHub Pages.

Create a branch for GitHub Pages deployment (for non-main branch deployment)


git checkout -b gh-pages
Push the branch to GitHub Pages


git push origin gh-pages
On GitHub (via web GUI):
Navigate to your repository → Settings → Pages → Select your branch (usually gh-pages) and set it as the source for GitHub Pages.


13. Managing Remotes
Handling remote repositories.

View all remote repositories


git remote -v
Change remote URL


git remote set-url origin <new_url>
Remove a remote


git remote remove origin


14. Deleting Repositories (Local and Remote)
Cleaning up repositories.

Remove the Git repository (keep files, remove .git folder)


rm -rf .git


Delete a remote repository
Done via the GitHub web interface (Settings → Danger Zone → Delete this repository).