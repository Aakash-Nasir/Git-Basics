# Git-Basics

'git init' ->  Powers your folder to be managed by git and initialises a new empty repository.
               It also creates a .git folder that has all relevant logic to manage versions of your project.

Working Area -> There can be a branch of files that are not currently handled by git.
                It means that changes or to be done in those files are not managed by git yet.
                  A file which is in working area is considered to be not in the staging area.
                  When we do git status and we see a bunch of untracked files 
                  then these are actually called  to be in the working area.

Staging area -> what  all files are going to be part of the next version that we will create .
                This staging area is the place where git knows what changes will be done from 
                the last version to the next version.

 Repository area:-> This area actually contains the details of all you previous registered versions. 
                     And the files in this area, git already manages then and knows their version history.

'git add <files> -> moves file from working area to staging area.

'git rm-cached <files> -> moves file back from staging area to working area.

'commit' -> commit is a particular version of the project. It captures a snapshot of the project's 
             staged changes and creates a version out of it.

'git commit'-> registers staging changes  to a commit.

 'git -log'-> list downs all the commits to the repository.
               if you want to exit out of git log prompt then press 'q' .

 'git restore <files> -> it moves all files changes from the staging area to be commited .
                        this can be useful , if we do  some  dirty piece of code and now no more want it . 
                        Instead of deleting every changes line by line,
                        we can restore it or you can say restore last clean version of the file.         0

'git restore --staged <files> ' ->  it removes files from  changes from staging area to working area.
                                     this only works if changes are in your staging area.

 Difference between git rm and git restore ->  If you want  to move the whole file back to the untracked state , then we do git rm, otherwise
                                               If we just want the changes to be moved in working area or staging area then we git restore.
 

 'git Difference commit1 commit2'->  Gives the difference of all file changes between two commit.

-- -> if we want to avoid opening a text editor like vim/nano to  add commit messege we can use this following commmand.
 git commit -m " <your commit messege> -> if we want to avoid opening a text editor 
 like vim/nano to add commit messege we can use this following commmand

 'git remote' ->  List down all the remote connection names.

 Remote connection -> It helps you to link two git repositories for uploading and downloading 
                         changes from each otherwise


'git remote add <name of remote>  <link of the  remote> :-> This command helps us to add a new link
                                                           to the remote repo and give a name to it.

 'git remote rm <name of remote> : This command deletes a remote connection.


 'git remote rename <oldname> <newname>' : This command rename the remote connection.

 NOTE:-> The name of the remote connection is always used to establish communication between the repositories.

 'git add <file1> <file2> <file3> ': This command will add multiple file changes together in the staging area.
 
 'git add .  :-> This command will add all files from working repositories to staging area 
 

 'git pull <remote name> <branch name> : Downloads latest changes from the branch of the mentioned remote in your local repo.
 
   ### GIT WORKFLOW
If you consider a file in your Working Directory, it can be in three possible states.

It can be staged. Which means the files with the updated changes are marked to be committed to the local repository but not yet committed.
It can be modified. Which means the files with the updated changes are not yet stored in the local repository.
It can be committed. Which means that the changes you made to your file are safely stored in the local repository.

git add is a command used to add a file that is in the working directory to the staging area.
git commit is a command used to add all files that are staged to the local repository.
git push is a command used to add all committed files in the local repository to the remote repository. So in the remote repository, all files and changes will be visible to anyone with access to the remote repository.
git fetch is a command used to get files from the remote repository to the local repository but not into the working directory.
git merge is a command used to get the files from the local repository into the working directory.
git pull is command used to get files from the remote repository directly into the working directory. It is equivalent to a git fetch and a git merge .

  ### RECOMENDED PRACTICE TO DO:

   - make changes
   - git add <file>
   - git commit
   - git pull
   - git push

   merge conflicts can occur if multiple people  try to make changes to the same file and ten collaborate.


   
