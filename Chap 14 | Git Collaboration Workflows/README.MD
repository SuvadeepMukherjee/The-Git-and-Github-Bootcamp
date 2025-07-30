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

## Feature Branches

- Rather than working directly on master/main, all new development should be done on **separate branches**
- Treat master/main branch as the official project history
- Multiple teammates can collaborate on a single feature and share code back and forth without polluting the master/main branch
  - Master/main branch won't contain broken code
- Specific teams and projects usually have their own branch naming conventions
  - Often you'll see branch names that include slashes like bug/fix-scroll or feature/login-form or feat/button/enable-pointer-events

## Merging Feature Branches

- At some point, the work on feature branches will need to be merged in to the master branch
- Option to merge to master branch
  - Merge at will, without any sort of discussion with teammates
  - Discuss with your team if the changes should be merged in
  - Pull Requests