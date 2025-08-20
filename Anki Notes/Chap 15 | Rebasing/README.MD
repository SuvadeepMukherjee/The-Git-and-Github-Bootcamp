# Chap 15 | Rebasing

Anki ➡️ 15-rebasing

#### Q1:What is rebasing ? 

**Solution**:

- If the master branch is very active , my feature branches history is muddied because of a bunch of merge conflicts
- If we rebase the feature branch onto the master branch we actually rewrite history and end up with a linear structure 
- This moves the entire feature branch so that it begins at the tip of the master branch 
  - i.e re-base-ing them at the tip of the master
- Rebasing rewrites history by creating new commits for each of the original feature branches ![rebasing](../../Assets/rebasing.png)
- We can also wait until we are done with a feature and then rebase the feature branch onto the master branch![00REBASING](/Users/suvadeep/Desktop/The Git and Github Bootcamp/Assets/00REBASING.png) 

#### Q2:How to rebase ? (To get a better understanding do a demo of rebase)

**Solution**:

Command 

```bash
# make sure you are at your feat branch

git switch feat

git rebase master 
```

- We already have tons of merge from master into feature branch but we want to cleanup the structure 
- we just want to have new changes from master to our feature branch without previous merging
- new commits are made on the feature branch on top of the master branch's tip (the master branch is unaffected)![00REBASING](../../Assets/00REBASING.png)

#### Q3:What is the golden rule of rebase ? 

**Solution**:

- **NEVER** rebase commits that have been **shared with others**
- If you have already pushed commits up to Github, DO NOT rebase them unless you are positive no one on the team is using those commits
- You do not want to rewrite any git history that other people already have. It's **a pain to reconcile the alternate histories**
  - Since you have commits that don't even exist in other's history, and they have commits that don't exist in yours (since you've rebased!)

#### Q4:How to handle conflicts during rebasing ? 

(To get a better understanding do a demo)

- Set up a test repository 
  - Create a folder called rebase-demo
  - Add a file called file.txt and add initial content on it 
  - commit it 
- Create a new feature branch 
  - git checkout -b "feature-branch"
  - echo "some feature content">>file.txt
  - git commit -am "Add feature content"
- Make more changes to the main branch
  - git switch master
  - echo "Another line in main">>file.txt
  - git commit -am "update in main" 

**Solution**:

1. Resolve the conflict in your files
2. `git add <conflicted-files>` to mark them as resolved
3. run `git rebase --continue`

Just follow the bash instruction if you forget what to do . 