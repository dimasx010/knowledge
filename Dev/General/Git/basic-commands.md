# Basic commands Git

## General

Today, Git is by far the most widely used modern version control system in the world. Git is a mature and actively maintained open source project originally developed by Linus Torvalds, the famous creator of the Linux operating system kernel, in 2005. A staggering number of software projects rely on Git for version control, including commercial and open source projects. Developers who have worked with Git are well represented in the talent pool available for software development, and the system works seamlessly across a wide variety of operating systems and IDEs (integrated development environments).

Git, which has a distributed architecture, is an example of a DVCS (distributed version control system). Instead of having a single space for the entire version history of the software, as is common in once-popular version control systems such as CVS or Subversion (also known as SVN), in Git, the working copy of each developer's code is also a repository that can hold the complete history of all changes.

![git](https://github.com/dimasx010/knowledge/assets/105082657/f30bcef5-e86f-47a1-9eed-c032c0672a39)

## Comandos basicos

-  Initialize the git project. 
```git
git init
```
-  Add a file. 
```git
git add file.txt
```
-  Submit changes to the commit stage. 
```git
git commit -m "text message"
```
-  See the changes that have been added. 
```git
git diff --stated
```
-  Show all the commits we have made in conjunction with an alphanumeric string. 
```git
git log --oneline 
```
-  Show the branch we are in, if we are in the main branch we will see the word main, and we will also have a list of branches created. 
```git
git branch 
```
-  Delete branch. 
```git
git branch -D branch_name
```
-  Create a branch, and the text would be equal to the name of the branch and we make the switch to it. 
```git
git checkout -b branch_name
```
-  Change branch. 
```git
git checkout nombre_rama
```
-  Bring the changes from the secondary branch named "branch-b" to the branch we are on. 
```git
git merge branch-b
```
-  Upload changes to remote repos. 
```git
git push
```
-  We download the data from the branch we indicated. 
```git
git pull origin branch_name
```
-  Declare trusted directories. 
```git
git config --global --add safe.directory '%(prefix)//route'
```
-  Clone Project. 
```git
git clone -b master URL_PROJECT
```
-  List executed configurations. 
```git
git config --list
```
-  Send request to remote repo. 
```git
git request-pull -p origin/main
```
-  Discarding changes that have been made to the working directory. 
```git
git checkout
```
-  Removes a remote repo routing. 
```git
git remote remove origin
```

-  Removes all branch of local repository least main. 
```git
$ git branch | grep -v "main" | xargs git branch -D
```

## References
- https://www.atlassian.com/es/git/tutorials/what-is-git
