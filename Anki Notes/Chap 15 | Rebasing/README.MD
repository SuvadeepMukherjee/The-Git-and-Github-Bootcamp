# Chap 15 | Rebasing

Anki ➡️ 15-rebasing

#### Q1:What is rebasing ? 

**Solution**:

- If the master branch is very active , my feature branches history is muddied because of a bunch of merge conflicts
- If we rebase the feature branch onto the master branch we actually rewrite history and end up with a linear structure 
- This means the entire feature branch so that it begins at the tip of the master branch 
  - i.e re-base-ing them at the tip of the master
- Rebasing rewrites history by creating new commits for each of the original feature branches ![rebasing](../../Assets/rebasing.png) 