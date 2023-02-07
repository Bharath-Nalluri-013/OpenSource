
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




```

3. Choose an already existing branch and use `git diff BRANCH_NAME` to view the differences from a branch and the current branch. Summarize the difference from master to the other branch.

```


```

4. Write a command sequence to merge the branch that is not the master branch into `master`.

```


```


5. Write a command (or sequence) to (i) create a new branch called `math` (from the `master`) and (ii) change to this branch.

```


```
   
6. Edit B.py adding the following source code below the content you have there.
```
print 'I know math, look:'
print 2+2
```

7. Write a command (or sequence) to commit your changes.
```


```

8. Change back to the `master` branch and change B.py adding the following source code (commit your change to `master`):
```
print 'hello world!'
```

9. Write a command sequence to merge the `math` branch into `master` and describe what happened.
```


```
   
10. Write a set of commands to abort the merge.
```


```
   
11. Now repeat item 9, but proceed with the manual merge (editing B.py). All implemented methods are needed. Explain your procedure.
```


```

12. Write a command (or set of commands) to proceed with the merge and make `master` branch up-to-date.
```


```

13. Complete Part 2. Then, come back here and answer the following:
Report your experience of submitting the Part 2. Please, include the steps you followed, the commands you used, and the hurdles you faced (within the file you created for the **Part 1**).
```


