# Chap 10 | Undoing Changes & Travelling back in time

#### Q1:How can we view the contents of an old commit , poke around , view the files etc ? 

**Answer**:

- `git log --oneline`
- `git checkout commit-hash`

Note ➡️ This will put us in detached HEAD

#### Q2:What is detached HEAD ? 

**Answer**:

- HEAD is a pointer to the current branch reference 
- The branch reference is a pointer to the last commit made on a particular branch![zzzz-detached-head-1](/Assets/zzzz-detached-head-1.png)

- When we checkout a particular commit , HEAD points at that commit rather than at the branch pointer 

```bash
git checkout d8194d6
```

![zzzzz-detached-head-2](../../assets/zzzzz-detached-head-2.png)