# Chap 6 | Working with branches 

Anki Tag: 06-working-with-branches

#### Q1:What is the master branch ? 

**Answer**:The default branch name is master ,  GitHub has renamed the  master name to main while git has kept the name master 

#### Q2:What is a HEAD  ? 

**Answer**:

- Each branch has a branch reference pointing to where we left called branch pointer . A branch pointer is where a branch currently is . Head is a reference to a branch pointer 
- HEAD is simply a **pointer** that refers to the **current "location"** in your repository. It points to a particular branch reference
- Like many different bookmarks in a book, only one position can be opened at a time

![head](../../Assets/head.png)

#### Q3:What is the git command to view existing branches ?

**Answer**:

`git branch`

Look for the * which indicates the branch we are currently on 

#### Q4:If git branch shows us in full screen all the branches then what is the command to exit  ? 

**Answer**:

Press `q` to exit

#### Q5:What is the  ways  to make a new branch based upon the current HEAD and then switch to it ?

**Answer**:

- Use `git branch <branch-name>` to make a new branch based upon the current HEAD .This just creates the branch , it does not switch you to that branch (the HEAD stays the same). Once you have created a new branch, use `git switch <branch-name>` to switch to it
- Another way of switch: `git checkout <branch-name>`(This also only switches the branch does not create it) , 
- Note ➡️ git checkout  does a million additional things

#### Q6:Create a new branch and directly switch to that branch in 2 different ways 

**Answer**:

Create and switch to a branch **at the same time**: `git switch -c <branch-name>` or `git checkout -b <branch-name>`

- `-c` stands for create
- `-b` stands for branch

#### Q7:If you switch branches with unstaged changes when will we  get an error, when will we not get an error  and what are the ways to fix the error ? 

**Answer**:

- If you switch branches with unstaged changes we will get an error if the unstaged changes are not a new file(there are conflicts between the branches) 

- Two options of fixing the error

  - commit it 
  - stash it 

  We will not get an error if the unstaged changes are  in a new file(there are no conflicts between the branches) and the new file will be moved to the new branch 

#### Q8:What is the command to delete a branch ? 

**Answer:**

Use `git branch -d <branch-name>`

- You cannot be in that branch if you want to delete it
- You cannot delete a branch thats not fully merged , we can confirm we want to delete it with the D flag i,e `git branch -D <branch-name>`

#### Q9:What is the command to rename a branch ? 

**Answer**:

Use `git branch -m <new-branch-name>` to rename a branch, 

Note  ➡️  we must be on the   the branch we want to rename

