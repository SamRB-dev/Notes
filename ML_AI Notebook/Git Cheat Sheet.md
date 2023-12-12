**Git Cheat Sheet**
=======================

**1. Getting Started**
------------------------

- Initialize a new Git repository:
```
git init
```

- Clone an existing repository:
```
git clone <repository_url>
```

**2. Basic Commands**
----------------------

- Check status of the repository:
```
git status
```

- Add changes to the staging area:
```
git add <file_name>   # Add specific file
git add .             # Add all changes
```

- Commit changes:
```
git commit -m "Commit message"
```

- View commit history:
```
git log
```

**3. Branching**
-----------------

- Create a new branch:
```
git branch <branch_name>
```

- Switch to a branch:
```
git checkout <branch_name>
```

- Create and switch to a new branch:
```
git checkout -b <branch_name>
```

- Merge a branch into the current branch:
```
git merge <branch_name>
```

- Delete a branch:
```
git branch -d <branch_name>
```

**4. Remote Repositories**
---------------------------

- Add a remote repository:
```
git remote add <remote_name> <repository_url>
```

- Push changes to a remote repository:
```
git push <remote_name> <branch_name>
```

- Pull changes from a remote repository:
```
git pull <remote_name> <branch_name>
```

- Fetch changes from a remote repository:
```
git fetch <remote_name>
```

**5. Undoing Changes**
-----------------------

- Discard changes in a file:
```
git checkout -- <file_name>
```

- Discard all local changes:
```
git reset --hard HEAD
```

- Revert a commit:
```
git revert <commit_hash>
```

- Amend the last commit:
```
git commit --amend
```

**6. Advanced Techniques**
--------------------------

- Interactive rebase:
```
git rebase -i <commit_hash>
```

- Cherry-pick a commit:
```
git cherry-pick <commit_hash>
```

- Stash changes:
```
git stash
git stash apply
```

- Resolve merge conflicts:
```
git mergetool
```

- Reset a branch to a specific commit:
```
git reset <commit_hash>
```

- Squash multiple commits into one:
```
git rebase -i HEAD~<number_of_commits>
```

**7. Git Aliases**
-------------------

- Create a Git alias:
```
git config --global alias.<alias_name> '<command>'
```

Example:
```
git config --global alias.co 'checkout'
```

**8. Additional Tips**
----------------------

- Ignore files and directories:
Create a `.gitignore` file and list the files/directories to be ignored.

- View Git configuration:
```
git config --list
```

- Show changes introduced by a commit:
```
git show <commit_hash>
```

- View the differences between branches:
```
git diff <branch1> <branch2>
```

- Amend author/committer information:
```
git commit --amend --author="Author Name <email@example.com>"
```

- Create and apply patches:
```
git format-patch <commit_range>
git apply <patch_file>
```

- Git tags:
```
git tag <tag_name>
git push origin <tag_name>
```

