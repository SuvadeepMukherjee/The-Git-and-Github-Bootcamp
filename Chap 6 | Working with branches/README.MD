## Chap 6 | Working with branches 

**Branches Introduction**

1. When we make a commit , each commit gets a hash (a unique identifier that corresponds to the commit) and each commit references at least one parent commit
2. Contexts: on large projects, we often work in multiple contexts
   - You're working on 2 different color scheme variations for your website at the same time, unsure of which you like best
   - You're also trying to fix a horrible bug, but it's proving tough to solve. You need to really hunt around and toggle some code on and off to figure it out
   - A teammate is also working on adding a new chat widget to present at the next meeting. It's unclear if your company will end up using it
   - …etc
3. If we all do these in a linear way, it would be impossible
   - How could we be working on two separate things, where some of which break other people's code?

4. Branches

   - Alternative timelines for a project

   - They enable us to create separate contexts where we can try new things, or even work on multiple ideas in parallel

   - If we make changes on one branch, they do not impact the other branches, unless we merge the changes

<img src="../Assets/branch.png" alt="branch" style="zoom:33%;" />



**The Master Branch**:

The default branch name is **master**

- It is just the same as other branches

Many people designate the master branch as their "source of truth" or the "official branch" for their codebase, but that is left to you to decide

