
### Development workflow

Branches are one of the basic concepts of git. There is a main branch `master`, and new branches are created out of the main master branch. Every branch represents a feature you are working on, and it has different series of commits. Once a feature is complete, the new branch is `merged` into the master branch.

Branches allow us to work on more than 1 feature at the same time, thus helping us avoid mixing of commits. If during the process, there are useless commits added and the whole branch is messed up, you can easily delete the branch and create a fresh branch from the main `master` branch.

Note: **Never ever commit or rebase on your master branch**.

The development workflow goes like this :

1. Clone the repo.
2. Cd into the repo.
3. Currently, you are on your master branch. Now you need to add a file named `Your_Name.txt`, you should a create a new branch with any name of your choice(could be your name as well), with:    

    `git branch <branch-name>`    
    And then, checkout to the branch you created by:
    
    `git checkout <branch-name>`
    This brings you to your new branch \<branch-name>.
    
4. Now, open up your text editor, create a file named `Your_Name.txt`.In the file, you should add your name in the first line, and your email-id in the second line. When you have made the changes, `commit`.

    The process of commiting goes like this:
    
    `git status` : This shows the status of your files, i.e. it shows which files are present in the staging area and which are not.
    
    `git add <path/to/file>` : This adds the selected files to the staging area. To add, all the files to staging area, do `git add .`
    
    `git commit` : On doing this, a text editor opens up and you are asked to enter a commmit message. Commit message should be short (less than 50 characters), and should convey what change you have made. Keep the commit message as meaningful as possible.
    
5. You have successfully committed your changes. You can then push these changes to your remote repository by :
    `git push origin <branch-name>`.    
    Note that all these changes took place in your created branch \<branch-name> , and you can delete whatever changes you made by deleting the branch. The above command pushed youur code online to your github repository.
    
6. Go to github's online repository and you can see an option of `Compare and Pull request` against your recently pushed branches. Make a Pull request by entering a short meaningful message and a meaningful comment about what your pull request does.

**Collaborating with others on github**

Steps to create a pull request:
1) Fork the parent repo to your account.
2) Clone the repo, from your account, to your remote machine.
3) Use "$ git checkout <newbranchname>" to create a new branch and make changes you want.
4) Use "$ git commit -m <comments>" from your branch to commit changes.
5) Use "$ git push origin <branchname>" to push the changes to your repo.
6) Go to your Github account and create a pull request to the parent repo.
7) Party! you just created a pull request. 🙂

**When multiple users using at same time and you had forked the repo sometime in the past**
* This is for incorporating changes others had made into the repo***

1) cd into your remote repo dir.
2) Use "$ git remote add upstream <clone link of parent repo>"
3) Use "$ git fetch upstream" to pull changes made by others.
4) Use "$ git merge upstream/master" to merge the changes
