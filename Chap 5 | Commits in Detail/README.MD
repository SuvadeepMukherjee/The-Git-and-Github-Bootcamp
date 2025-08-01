## Chap 5 | Commits in Detail 

## **Atomic Commits**:

- When possible a commit should encompass a single feature , change or file 
- In other words , keep each commit focussed on a single thing 
- This makes it easier to undo or rollback changes later on 

## **Commit Messages**:

- Order the code base to change its behavior 
- Example ➡️ fix: handle null values in user input validation

## **Commit messages with git commit in Vim**:

1. i  ➡️  insert mode 
2. Enter Commit message
3. ESC ➡️ Leave insert mode 
4. :wq ⏎ ➡️  Exit VIM 

✅ **I Easily Eat Worms Quickly** ➡️`i`➡️Enter Commit Message ➡️ `ESC` ➡️ `:wq` ⏎

## **git log --oneline**:

We can write longer commits with *git commit* , when writing a commit message with `git commit`, we can use a concise one-sentence summary as the first sentence and then add a longer summary if necessary.This way we can use *git log --oneline* to display a concise git log 

## **Ammending Commits**:

- Suppose we just made a commit and then realized we forgot to include a file! or maybe we made a typo in the commit message that we want to correct 
- Rather than making a brand new seperate commit , we can redo the previous commit using `git commit --amend`

```bash
git commit -m "Some Commit"

git add forgotten_file (Add to staging area)

git commit --amend
```

Note ➡️ We have to write the new commit message in Vim 

## **Command to exit git log and git log --oneline** 

-  `q `

## **Ignoring Files**:

- We can tell Git which files and directories to ignore in a given repository using a .gitignore file 
- This is useful for files we never want to commit 
  - Secrets , API keys , credentials 
  - Operating System Files (Eg ➡️ .DS_Store on Mac)
  - Log Files
  - Dependencies and packages
- .gitignore 
  - Create a file called .gitignore in the root of a repository 
  - Inside the file , we can write patterns to tell Git which files and folders to ignore 
    - .DS_Store ➡️ ignore files named .DS_Store 
    - folderName/ ➡️ ignore an entire directory 
    - *.log ➡️ ignore any files with the .log extension 
- Use  [gitignore.io](http://gitignore.io) to get recommended starting place for .gitignore 





