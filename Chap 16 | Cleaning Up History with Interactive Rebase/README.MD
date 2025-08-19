## Chap 16 |Cleaning Up History with Interactive Rebase

There are two main ways to use the `git rebase` command

- as an alternative to merging ← Chap 15
- as a cleanup tool **← Chap 16**

## Interactive Rebase Introduction

1. We can use `git rebase` to rewrite history **before sharing them**

   - edit, rename, delete commits

   - change commit message

   - reorder commits

2. Running `git rebase` with the `-i` option will enter the interactive mode, which allows us to edit commits, add files, drop commits, etc.

   - Note that we need to specify how far back we want to rewrite commits

   - We are not rebasing onto another branch

   - Instead, we are **rebasing a series of commits onto the HEAD they currently are based on**

   - For example, `git rebase -i HEAD~4`

3. [Exercise](https://github.com/Colt/interactive-rebase-demo) to follow along