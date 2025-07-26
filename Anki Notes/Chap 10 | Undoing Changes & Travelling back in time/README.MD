# Chap 10 | Undoing Changes & Travelling back in time 

Anki ➡️ 10-undoing-changes-and-travelling-back-in-time

#### Q1:What we can do in detached Head ? 

**Answer**:

- We can examine the contents of the old commit , poke around , view the files etc 

#### Q2:How to reattach detached HEAD ? 

**Answer**:

- Leave and switch back to wherever you were using `git switch -` or move to a particular branch using `git switch <branch_name>`
- Create a new branch and switch to it .You can now make and save changes since HEAD is no longer detached

#### Q3:How can we view a particular commit ? 

**Answer**:

- `git log --oneline` ➡️ Get the commit hash(First 7 digits)
- `git checkout <commit-hash>` (First 7 digits)

Note ➡️ We will be in detached HEAD in this state 

#### Q4:What is detached HEAD ? 

**Answer**:

- Usually HEAD points to a specific branch reference rather than a particular commit 
  - HEAD is a pointer to the current branch reference 
  - The branch reference is a pointer to the last commit made on a particular branch ![01-head](../../Assets/01-head.png)  

Detached HEAD ➡️ 

- When we checkout a particular commit , HEAD points at that commit rather than at the branch pointer 

  ```bash
  git checkout d8194d6
  ```

  ![01-detached-head](/Users/suvadeep/Desktop/The Git and Github Bootcamp/Assets/01-detached-head.png)



