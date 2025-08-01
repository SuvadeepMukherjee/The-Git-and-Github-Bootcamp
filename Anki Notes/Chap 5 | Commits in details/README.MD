## Chap 5 | Commits in details 

Anki Tag ➡️ 05-commits-in-details

#### Q1: How should commits be and how should commit messages be ? 

**Answer**:

- Commits should be atomic (keep each commit focussed on a single thing)
- Commit messages must be like "ordering the code base to change behavior"

#### Q2:How to write longer commit messages with git commit in Vim ? 

**Answer**:

1. i ➡️ insert mode 
2. Enter Commit Message 
3. ESC ➡️ Leave insert mode
4. :wq ⏎ ➡️ Leave insert mode 

✅ **I Easily Eat Worms Quickly**
 → `i` → Enter Commit Message →  `ESC` → `:wq`
 → Insert → Escape → Save & Exit

#### Q3: We can write longer commit messages with git commit and then write the commit message in vim , when writing the commit message we can use a concise one-sentence summary as the first sentence and then add a longer summary if necessary .This way we can use _______ to display a concise git log 

**Answer**:

`git log --oneline`

#### Q4:Suppose we just made a commit and then realized we forgot to include a file! or maybe we made a typo in the commit message that we want to correct, Rather tham making a brand new seperate commit , we can redo the previous commit using ______

**Answer**:

```bash
git commit -m "Some Commit"

git add forgotten_file (Add to staging area)

git commit --amend
```

 Note ➡️ We have to write the new commit message in Vim

#### Q5:What is the command to exit git log and git log --oneline ? 

**Answer**:

- q 

##### Q6: We tell Git which files and directories to ignore in a given repository using a _____ file 

**Answer**: 

`.gitignore`