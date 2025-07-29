## Chap 12 | Fetching & Pulling

Anki ➡️ 12-fetching-and-pulling

#### Q1:What is a remote tracking branch ? 

**Answer**:

When we clone a repo to our local machine from Github, we'll have two branch reference

- **Regular branch reference**: which we can move around
- **Remote Tracking Branch**: a reference to **the state of the master branch on the remote**. I can't move this myself
  - It's like a bookmark pointing to the last known commit on the master branch on origin![zz-remote-tracking-branch](../../Assets/zz-remote-tracking-branch.png)

- At the time you last communicated with this remote repository, here is where x branch was pointing
- They follow this pattern `<remote>/<branch>`
  - `origin/master` references the state of the master branch on the remote repo named origin
  - `upstream/logoRedesign` references the state of the logoRedesign branch on the remote named upstream (a common remote name)

#### Q2:How to view the remote branches our local repository knows about ? 

**Answer**:

`git branch -r`

#### Q3:How can we checkout on these remote branch pointers ? 

**Answer**:

- We can checkout on these remote branch pointers using `git checkout origin/master`

Note ➡️ This will put us in detached HEAD