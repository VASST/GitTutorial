# Welcome to the GiTorial


In this tutorial we are going to learn how to work collaboratively using Git.

## Software Installation

#### Git
You should have installed git. If you have not done so, please check the following link for installation instructions regarding your specific platform:

http://git-scm.com/book/en/v2/Getting-Started-Installing-Git


### GitHub client

https://windows.github.com/
https://mac.github.com/

#### Comparing versions

If you are using windows we recommend you to install winmerge:

http://winmerge.org/

Or meld (linux, mac, windows):

http://meldmerge.org/


* * * 
##### Getting started with GitHub

1. Create a GitHub account here:
 
    https://github.com/ 

2. Let us know what your username is so we can add you as a contributor to the novel repository

* * * 
##### Creating a local repository to work in the novel
 
3. Create a folder in your computer and name it **novel**. This folder will allow you to synchronize your changes with any remote changes (this repository).
 
4. Let's create a local git repo. Type:
 
  ```
  git init
  ```

5. Now let's add the remote (this repo) to which you will be updating:

  ```
  git remote add common https://github.com/VASST/novel
  ```
  where common is the name given to the remote repo and the url corresponds to its location.

6. Now let's **pull** the remote repo into your local folder. Type:

  ```
  git pull common master
  ```
  
  In this case *master* indicates the remote *branch* that you will be pulling from. This branch is *master* by     
  default.

6. You will be asked for your GitHub user and password. Please enter them.

7. At this point you should have a copy of the remote repository in your **novel** folder. Please go ahead and check that you have the files novel.txt, README.md and .gitignore. We will be working on **novel.txt**

8. Go ahead and open **novel.txt**. This file contains a draft for a thriller novel. At this point each one of you have a copy of the current version of the novel.

* * * 
##### Working on your local copy of the novel

9. Now let's do something interesting. You have several options here (please select only one):

  + correct typos
  + change the male character demand
  + change the ending
  + change the scenario
  + change the murder weapon
 
10. Once you have finished, go ahead and save your file. At this point, the file that you have in your computer looks different from the remote shared file. Git is aware of these changes. Type:

  ```
  git status
  ```
  **git status** tells you what changes have occured locally.

11. Git tells you that your copy of the novel has been modified. Let's commit our changes:

  ```
  git add novel.txt
  git commit -m '<describe the changes that you made in a sentence here>'
  ```
  **git add** allows you deciding which changes in your current working version you want to commit to your local
  repository. These changes are added to a *staging area*
  
  **git commit**, takes everything that has been added to the staging area to execute the commit. 

* * *   
##### Working with local versions

  Each commit has anID (identifier) which appears right after the commit is performed (e.g. 74dca64). As a matter of 
  fact you can retrieve the history of commits by typing:

  ```
  git log
  ```

  And if you are only interested in knowing about the last commit you can do so with:

  ```
  git log -n 1
  ```

  If later on you regret having commited your changes, you can reset to a previous state with:

  ``` 
  git reset --hard <commit-id>
  ```
  
  With this command you will have a slate clean reset to this point in time and you will not be able to go back to any
  future commits.

  If you are only interested in taking a look at how your novel looked like at a particular point in time without
  losing any subsequent commits, you must use **git checkout** instead:

  ```
  git checkout <commit-id>
  ```

##### Sharing your changes with the writing team

12. The changes you have implemented are *local*. This is, you have updated your local version of **novel.txt**, now
    if you want to share your changes with the editorial team, you need to *push* your changes to the remote      
    repository. You do that with:

    ```
    git push common master
    ```
    
    Here you are indicating to Git to push your *master* branch (because we have not created local branches, we are by     default in the *master* local branch) to the master branch in the remote known as *common* (the common   
    repository).
    
    If you wanted to push to a different branch in the remote (in case we had more than one branch) you could indicate     which branch you are interested in pushing your changes to with:
    
    ```
    git push common local_branch:remote_branch
    ```
    
    
    
    

    
    
    





 
 
