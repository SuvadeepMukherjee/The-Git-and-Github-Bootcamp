## Reflogs - Retreiving Lost Work

Anki ➡️ 19-reflogs

#### Q1:What is reflogs ? 

**Solution**:

- short for reference logs
- Git keeps a record of when the tips of branches and other references were updated in the repo

#### Q2:What are the limitations of reflogs ? 

**Solution**:

- Git only keeps reflogs on your local activity (They are not shared with collaborators)
- Reflogs also expire .Git cleans out old entries after around 90 days though this can be configured

#### Q3:Explain the git reflog command 

**Solution**:

- The **git reflog** command aceepts subcommands show , expire , delete and exists .show is the only commonly used variant and it is the default subcommand 
- **git reflog show <references>** will show the log of a specific reference(it defaults to HEAD)
  - `git reflog show HEAD`
  - `git reflog show main`  ➡️ view the logs for the tip of the main barnch 

Note ➡️ We have the <reference>{qualifier} tags which indicate a particular entry in the reflog

![git-reflog-1](../../Assets/git-reflog-1.png) 

#### Q4:How can we see the following 

- The reflog logs in HEAD from 10 logs till the end
- The state of the codebase of HEAD at 2nd log in reflog
- The diifference in HEAD reflog at 0 and 5 

**Solution**:

We can access specific git refs using `name@{qualifier}`. We can use this syntax to access specific ref pointers and can pass them to other commands including `checkout`, `reset`, and `merge`

Commands : `git reflog HEAD@{10}`, `git checkout HEAD@{2}`, `git diff HEAD@{0} HEAD@{5}`

#### Q5:How can we see the following ? 

- reflog entries in the master branch one week ago
- checkout at the bugfix branch based on the reflog entry 2 days ago 
- the diff between the reflog entries now and yesterday at the main branch 

**Solution**:

- **Timed References**: every entry in the reference logs has a **timestamp** associated with it
- We can **filter** reflogs entries by time/date by using time qualifiers like
  - 1.day.ago
  - 3.minutes.ago

For example:

```bash
git reflog show master@{one.week.ago}
git checkout bugfix@{2.days.ago} 
git diff main@{0} main@{yesterday}
```

#### Q6:Recover a lost commit with git reflog

Follow the following steps 

-  add a file and commit it with initial commit , make the console log also initial commit 
- in the same file add `console.log("commit 1")` and the commit also commit 1
- in the same file add `console.log("commit 2")` and the commit also commit 2
- in the same file add `console.log("commit 3")` and the commit also commit 3
- Now reset --hard back to commit 2 
- Your task is to recover the lost commit `console.log("commit 3")`

**Solution**:

First run `git reflog show master`![reflog-practise](../../Assets/reflog-practise.png)

Then run `git reset --hard master@{1}`![reflog-solution](../../Assets/reflog-solution.png)