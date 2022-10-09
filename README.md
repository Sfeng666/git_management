# git_management
common tricks for git managements
1. [Remove selected files from `.git` history](https://junyonglee.me/github/How-to-clean-up-git-repository/#cleaning-up-repo)  
  * `git filter-branch` to remove large files from the history
  `git filter-branch -f --index-filter 'git rm -r --cached --ignore-unmatch "data/env_data" "*.txt" "*.html"git' --prune-empty --tag-name-filter cat -- --all`   
  * Cleaning up repo   
  `rm -Rf .git/refs/original`   
  `rm -Rf .git/logs/`   
  `git gc --aggressive --prune=now`  
  * Updating remote repo    
   `git push origin --force --all`    
   `git push origin --force --tags`
