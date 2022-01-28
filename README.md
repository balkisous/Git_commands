# Git_commande
# Useful commands on git to know :

  --- Git push ---
  # Which files are modified
    o git status
      raccourci -> gst
 
  # To see the Logs / commits
    o git log
  
  # To add or remove files 
    o git add/rm files (*.c, *.h, ...)
    
  # To add commit
     o git commit -m "bla bla ..." 
  
  # To push localy
    o git push main/<branch>
    
  # To push in remote
    o git push origin main/<branch>
  
  
  --- Branch ---
  
  # Create a branch
    o git checkout -b <branch name>
    
  # Change branch
    o git checkout <branche name>

  # Rename a branch
    o git branch -m <old branch name> <new branch name>

  # Delete branch locally
    o git branch -d localBranchName

  # Delete branch remotely
    o git push origin --delete remoteBranchName
    
  --- Merge ---
  
  # How to Merge in another branch/and fix Merge Conflict
    Exemple you want merge your branch <parsing> in <main>
    1) -> Pull your repostory to be up to date : ~minishell<parsing> git pull 
    2) -> Then git status to see what is modified, then you add your files, commit and push remotly (with origin before branch name)
    3) -> Now you merge main in parsing : ~minishell<parsing> git merge origin main
  # if you have no merge conflict you can merge in main and push
       L->  ~minishell<parsing> git checkout main
            ~minishell<parsing> git merge origin parsing
            ~minishell<parsing> git push origin main
  # else if you have merge conflict 
      4)  -> change the files that have merge conflict in <parsing> branch
      5)  -> Then add the file, and commit in <parsing> branch
      6)  -> Now push in remotely in <parsing> branch
      7)  -> Re merge -> normally now it's okay to merge
      8)  -> Then merge in <parsing> branch : ~minishell<parsing> git merge origin main
      9)  -> No merge conflict, change branch : ~minishell<parsing> git checkout main
      10) -> now merge in main : ~minishell<main> git merge origin parsing
      11) -> You can push in main but since we have pushed in <parsing> branch we don't need to push in <main> branch : (optional) ~minishell<main> git push origin main
  
