# Chap 14 | Git Collaboration Workflows

## Centralized Workflow

- Everyone works on master/main branch, the most basic workflow possible
- It's straightforward and can work for tiny teams, but it has quite a few shortcomings
- If your current work is behind the remote work, you cannot push instead of pulling (merge) by `git pull` first
- If you have some problematic code and want to share that with your collaborators and get some advise, you have to pull down the remote work, merge, then push your code.
   Since there's only one branch, this could be problematic!
- The problem
  - Lots of **time** spent **resolving conflicts and merging** code, especially as team size scales up
  - No one can work on anything without disturbing the main codebase. How do you try adding something **radically different** in? How do you **experiment**?
  - The only way to collaborate on a feature together with another teammate is to push **incomplete code** to master. Other teammates now have broken code…