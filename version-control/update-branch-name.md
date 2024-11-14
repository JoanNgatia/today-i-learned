### Renaming Git Branches

Usually, git branch names provide context around the changes made in the branch. 
Here are the steps taken to rename the branches:

1. Rename the current branch
   ```bash
   $ git branch -m <newname>
   ```
2. Push the local branch and reset the upstream branch:
   ```bash
   $ git push origin -u <newname>
   ```
3. Delete the remote reference to the old branch name:
   ```bash
   git push origin --delete <oldname>
   ```
4. Voila 🚀
  
