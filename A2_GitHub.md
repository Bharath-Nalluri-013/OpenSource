
1. List all the branches in this repository and, for each branch, list the commits.

    - Use `git branch` to list the branches in this repository.
    - Use `git checkout` to explore each branch.
    - Use `git log --decorate` to explore the structure of commits.

```
1. Used "git branch" to find branches of this repositories
Branches in the repository: 2
Name of the branches: feature-foo and main
2. Used "git checkout" to navigate to main branch

3. To track commits, I used "git log --decorate" command
Upon running the command, we can see we have 3 commits in total.
3 Commits:
commit f67f266cf420735187053f10d32e2c0f7cbc5a43 (HEAD -> master)
Author: Igor Steinmacher <igorsteinmacher@gmail.com>
Date:   Fri Aug 24 15:30:05 2018 -0700

    Adding class B skeleton

commit 309b0d73ff9c2163591c9e96e307fe61b4c8f58a
Author: Igor Steinmacher <igorsteinmacher@gmail.com>
Date:   Fri Aug 24 15:27:16 2018 -0700

    Adding class A skeleton

commit 9c1eeb8901b0926ce7fa13cc6ce0a1876fc4179b
Author: Igor Steinmacher <igorsteinmacher@gmail.com>
Date:   Fri Aug 24 15:26:44 2018 -0700

    Creating all files (all empty)


(Please find result screenshot at https://github.com/Bharath-Nalluri-013/OpenSource/tree/A2_Github-Practice -- A2Q1.png)



```

2. Try `git log --graph --all` to see the commit tree. Paste the result here and write a paragraph to provide an interpretation of what you found.
```
Result after running the command "git log --graph --all" is as follows:
commit f67f266cf420735187053f10d32e2c0f7cbc5a43 (HEAD -> master)
Author: Igor Steinmacher <igorsteinmacher@gmail.com>
Date:   Fri Aug 24 15:30:05 2018 -0700

    Adding class B skeleton

commit 309b0d73ff9c2163591c9e96e307fe61b4c8f58a
Author: Igor Steinmacher <igorsteinmacher@gmail.com>
Date:   Fri Aug 24 15:27:16 2018 -0700

    Adding class A skeleton

commit 9c1eeb8901b0926ce7fa13cc6ce0a1876fc4179b
Author: Igor Steinmacher <igorsteinmacher@gmail.com>
Date:   Fri Aug 24 15:26:44 2018 -0700

    Creating all files (all empty)

E:\Spring 2023\Open Source Software Dev\A2 Git and Github\handson>git log --graph --all
* commit f67f266cf420735187053f10d32e2c0f7cbc5a43 (HEAD -> master)
| Author: Igor Steinmacher <igorsteinmacher@gmail.com>
| Date:   Fri Aug 24 15:30:05 2018 -0700
|
|     Adding class B skeleton
|
| * commit a70a8e9d3c5390e367028faf033f2a9ef03d2e91 (feature-foo)
|/  Author: Igor Steinmacher <igorsteinmacher@gmail.com>
|   Date:   Fri Aug 24 15:29:22 2018 -0700
|
|       Adding header of method foo()
|
* commit 309b0d73ff9c2163591c9e96e307fe61b4c8f58a
| Author: Igor Steinmacher <igorsteinmacher@gmail.com>
| Date:   Fri Aug 24 15:27:16 2018 -0700
|
|     Adding class A skeleton
|
* commit 9c1eeb8901b0926ce7fa13cc6ce0a1876fc4179b
  Author: Igor Steinmacher <igorsteinmacher@gmail.com>
  Date:   Fri Aug 24 15:26:44 2018 -0700

      Creating all files (all empty)


Upon looking at the tree above, I can understand,
Git log is used to list all the commits for the repository. Git log has many options and one of them is graph. git log --graph is used to show graphical representation of the commit history. This representation is shown on the left hand side of the output.
out of these commits, each * represents single commit commits and '/' this symbol indicates that the commit is in child branch that is "feature-foo". Others are the main branch commits.


(Please find result screenshot at https://github.com/Bharath-Nalluri-013/OpenSource/tree/A2_Github-Practice -- A2Q2.png)



```

3. Choose an already existing branch and use `git diff BRANCH_NAME` to view the differences from a branch and the current branch. Summarize the difference from master to the other branch.

```
--> git diff branch_name compares and gives us differences between the branch that we are currently on and the branch_name we entered. 
--> In our case, we are in our main branch. So we compared main branch with feature_foo branch.
--> Upon running the command "git diff feature-foo", we can see :
diff is comparing A.Java files from both the branches.
--- indicates one of the branches java files and +++ indicates java file from another comparing branch.
--- is also color coded in red and +++ is color coded in green which shows what are the changes in both the java files. This color coding helps in easily identifying differences between the context in files.


(Please find screenshot for the color coded output on https://github.com/Bharath-Nalluri-013/OpenSource/tree/A2_Github-Practice -- A1Q3.png)

```

4. Write a command sequence to merge the branch that is not the master branch into `master`.

```
Commands to merge a non-master branch into master branch:
git checkout master      #enter master branch
git merge branch_name    #merge branch branch_name into master branch

Since the repository we are working is on local machine, we don't need to worry about remote repositories. If it is a remote repository, we have fetch recent changes from remote repository and also push changes to remote repository.

```


5. Write a command (or sequence) to (i) create a new branch called `math` (from the `master`) and (ii) change to this branch.

```
Commands to do this part of the question:
git checkout master    #Naviagtes to master branch
git branch math        #To create a new branch called 'math'
git checkout math      #To change to created branch

We can also do this in one step: git checkout -b math
(I assumed we are already in master branch, if we are not in master branch, we have to move to master branch first (using git checkout master) and then run above commands.)

(Please find command screenshots on https://github.com/Bharath-Nalluri-013/OpenSource/tree/A2_Github-Practice A2Q5.png)

```
   
6. Edit B.py adding the following source code below the content you have there.
```
Lines to be added:
print 'I know math, look:'
print 2+2

Commands to make above changes:
git checkout master
git ls-files      
(#here open the file that you need from all files in the branch on your local machine, in our case its B.java,make changes which is adding lines, save file and close editor)
git add B.java

(Please find command screenshots on https://github.com/Bharath-Nalluri-013/OpenSource/tree/A2_Github-Practice A2Q6.png)

```

7. Write a command (or sequence) to commit your changes.
```
git commit -m "Two Additional lines were added at the end to the file on main branch."
(#here commit new changes with a message)

(Please find command screenshots on https://github.com/Bharath-Nalluri-013/OpenSource/tree/A2_Github-Practice A2Q7.png)
```

8. Change back to the `master` branch and change B.py adding the following source code (commit your change to `master`):
```
Changes to be made:
print 'hello world!'

Commands to do that:
git checkout master (#changes current branch to master)
git ls--files (#lists all the files, select B.py file and edit in text editor and add print 'hello world!' line)
git add B.py
git commit -m "One Additional lines was added at the end to the file on math branch."

(Please find command screenshots on https://github.com/Bharath-Nalluri-013/OpenSource/tree/A2_Github-Practice A2Q8.png)


```

9. Write a command sequence to merge the `math` branch into `master` and describe what happened.
```
Commands to merge math into master:
git checkout master
git merge math

Explanation:
You have to enter master branch first to merge. So we used git checkout master.
Second step is to merge math branch(which we created in q5). we use "git merge" math to merge.
When we run this we run into a confiict. Because there are differences in B.java in main branch and B.java in math branch. So in order to succesfully merge, we have to clear the conflivt by accepting the changes. 
(I attached a screenshot of conflict at https://github.com/Bharath-Nalluri-013/OpenSource/tree/A2_Github-Practice A2Q9_error.png)
Change these conflicts, save the file and merge again for successful merge.
((Please find command screenshots on https://github.com/Bharath-Nalluri-013/OpenSource/tree/A2_Github-Practice A2Q9.png))


```
   
10. Write a set of commands to abort the merge.
```
To abort a merge: git merge --abort
#Aborts latest merge.

```
   
11. Now repeat item 9, but proceed with the manual merge (editing B.py). All implemented methods are needed. Explain your procedure.
```
Commands:
git checkout master
git merge math         #here you get conflicts
cat B.java             #shows you conflicts, clear the conflicts
git add B.java
git commit -m "conflicts cleared!"

Explanation:
--> First command is to checkout on master branch. 
--> Next step, we will try to merge math branch to main branch. When we run this, it throws conflicts, you can either see conflicts by opening the B.java file in an editor or type "cat B.java" to show contents in B.java file.
--> Now that you opened B.java file in an editor, clear all the conflicts and save the file.
--> Come back to git cmd, add B.java file by running command "git add B.java"
--> Commit these changes in the next command.

(Please find command screenshots on https://github.com/Bharath-Nalluri-013/OpenSource/tree/A2_Github-Practice A2Q11.png)
```

12. Write a command (or set of commands) to proceed with the merge and make `master` branch up-to-date.
```
git checkout master
git merge math
#This shows the output "Already upto date"

OR 

git rebase master #used to keep master branch up to date


(Please find command screenshots on https://github.com/Bharath-Nalluri-013/OpenSource/tree/A2_Github-Practice A2Q11.png)
```

13. Complete Part 2. Then, come back here and answer the following:
Report your experience of submitting the Part 2. Please, include the steps you followed, the commands you used, and the hurdles you faced (within the file you created for the **Part 1**).
```
Experience submitting Part 1 of this assignment:
1. I had experince with GitHub when I was in my UnderGrad. I created a repo and uploaded some files from my local machine to host them.
2. I know how to use GitHub but I did not use git commands.
3. For the questions that I am not sure with git, I referred slides from the lecture, browsed online to get more info about some commands.
4. There were plenty of resources and explanations for a specific command. I used those references for commands like git log graph, git ls files and so on.
5. Talking about the challenges for this task, I was confused when I see remote branches while listing the branches for the repository. I had to know more information about remote branches and the ways to deal remote branches. I cloned local repository into GitHub desktop and thats where issues started. I figured out ways to deal with remote branches as well. I also had difficulty in clearing the conflicts, how to compare and clear. Upon practice, I was able to figure out things for conflicts.
One useful resources I think useful for this assignment:
https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging

Experience submitting Part 2 of this assignment:
GitHub pullrequest is most important and I previously had some experince in this. So I am able to do this task with no problems.
For the paper I reported for this task is from google scholar. I was in a process of understanding importance of Pull Requests and this paper helped me understand it.
I have not faces any challenges with task 2 for the assignment. May be I should be more familiar with formatting md file in a github.

