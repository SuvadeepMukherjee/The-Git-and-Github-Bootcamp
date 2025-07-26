# Chap 7 | Merging Branches 

## Introduction to Merge 

- Two basic concepts 
  - We merge branches , not specific commits 
  - We always merge to the current HEAD branch 
- Two basic steps
  - Switch to or checkout the branch you want to merge the changes into(the receiving branch)
  - Use `git merge` to merge changes from a specific branch into the current branch 

## Fast-Forward Merge 

- A fast-forward merge can occur when there is a linear path from the current branch tip to the target branch 
- Instead of actually merging the branches , all Git has to do to integrate the histories is move (i.e "fast forward") the current branch tip up to the target branch tip 

```bash
# For example, merge the bugfix branch into master

git switch master
git merge bugfix
```

Visualization 

<img src="../Assets/FF1.png" alt="FF1" style="zoom:25%;" />

<img src="../Assets/FF2.png" alt="FF2" style="zoom:25%;" />

<img src="../Assets/FF3.png" alt="FF3" style="zoom:25%;" />

Actually it looks like this , this is called a fast-forward

![FF-real](../Assets/FF-real.png)

## Not All Merges Are Fast-Forwards!

- Imagine one of your teammates merged in a new feature or change to master while you were working on a branch 
- ![NFF](../Assets/NFF.png)

- Two scenarios 
  - There is no conflict  ➡️ git can do the merge for us automatically 
  - There is a conflict , eg your teammates edit line 45 on master and you also edit line 45 on bugfix, which edit will win ? 

- The no conflict scenario

  - Rather than performing a simple fast forward , git performs a "merge commit"
  - We end up with a new commit on the master branch
  - Git will prompt you for a message
  - ![no-conflict](../Assets/no-conflict.png)

  - That merge commit will have two parent commits 
  - ![](../Assets/merge-no-conflicts.png)

## Merge Conflicts

- Depending on the specific changes you are trying to merge , Git may not be able to automatically merge 
  - This results in merge conflicts, whivh we need to manually resolve 
- When you encounter a merge conflict ,Git warns you in the console that it could not automatically merge ![merge-conflict](../Assets/merge-conflict.png) 

- It also changes the contents of our files to indicate the conflicts that it wants you to resolve
  - The content from your current HEAD (the branch you are trying to merge content into) is displayed between the <<<<<<< HEAD and =======
  - The content from the branch you are trying to merge from is displayed between the ======= and >>>>>>> symbols.![merge-conflict-console](../Assets/merge-conflict-console.png)

- Resolving conflicts 
  - Open up the file(s) with merge conflicts
  - Edit the file(s) to remove the conflicts.Decide which branch's content you want to keep in each conflict.Or keep the content from both 
  - Remove the conflict "markers" in the document
  - Add your changes and then make a commit! 
