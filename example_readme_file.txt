git example readme file 


1. To set the user account 
	git config --global user.email "sudhamadhavi814@gmail.com"
	git config --global user.name "Madhavi"
2. To check the user account details
	git config --global user.email 
	git config --global user.name 

In remote repository,

1. create a new repository in GitHub (https://github.com/)
2. click New->give repository name->provide some description->select 	private or public->select add readme file->create repository.




Creating a local repository and pushing it to remote


1. create a repository folder in local
2. add required code
3. open git bash and move to that repo
4. enter git status (to check the status)
5. enter git init (Initialize the git repository)
6. .git folder will be generated in repo folder
7. ls -la (to check the list of files in the repo) 
8. git add filename (to add the files to the repo)
9. git commit -m "commit message" (to commit the added files)
10. git log   (displays the logs which are committed )
11. git remote -v  (to check URL in your remote configuration)
12. If there is a typo or if it's not correct, update the URL
	Ex: git remote set-url origin https://github.com/Madhavi793/gitexample.git
13. git push --set-upstream origin master ( if it's the first time pushing, complete the authentication process and changes pushed to origin/Master)
14.  git fetch origin (Fetch the latest changes from the remote)
15. git merge origin/master (Merge the changes into your local branch)
16. git pull origin master (which is a combination of fetch and merge)

To push your local changes to the remote repository (origin), you can use the git push command. This command sends your local commits to the remote repository.
17. git branch (check which branch you are currently on, The current branch will have an asterisk (*), example : *master)
18. git push origin master(push your local master branch to the origin remote)
	If you are on a different branch, replace master with the name of the branch you're working on

To discard changes

Discard Unstaged Changes (Local Modifications)
19. git checkout -- <file>  (to discard changes in a specific file, This will revert the file back to its state in the last commit.)

	git restore --source=HEAD -- .(Discard All Unstaged Changes)
	This will discard all modifications to tracked files in your working directory and reset them to their last committed state (i.e., HEAD).

Discard Staged Changes (Changes Added with git add)
git reset <file>
This removes the file from the staging area, but it won’t discard the changes in the file; it just unstages them.

To discard staged changes (reset the file back to its last committed state), use:

git checkout -- <file>


 Discard All Local Changes (Unstaged and Staged)
If you want to discard both unstaged and staged changes (i.e., reset the entire working directory to match the last commit), use:

git reset --hard HEAD

git reset --hard as it will permanently discard changes, and they won’t be recoverable unless they were committed or you have backups.

Revert to a Specific Commit
If you want to discard all changes and reset the branch to a specific commit, use:

git reset --hard <commit>
Replace <commit> with the commit hash you want to revert to. You can find the commit hash by running git log.


Steps to commit the file removal:

Stage the file removal:   git rm "filename"   
Commit the file removal:  git commit -m "Remove 'git example readme file.txt'"
Push the commit to the remote repository: git push origin master

If the file was already deleted manually or moved outside of your repository, and Git is still tracking it as "deleted" in your working directory, but the file no longer exists on your file system.
Force stage the deletion: git rm --cached "filename"





