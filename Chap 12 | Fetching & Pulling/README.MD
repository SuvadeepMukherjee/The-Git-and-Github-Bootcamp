## Chap 12 | Fetching & Pulling

## Remote Tracking Branch

- When we clone a repo to our local machine from Github, we'll have two branch reference

  - **Regular branch reference**: which we can move around
  - **Remote Tracking Branch**: a reference to **the state of the master branch on the remote**. I can't move this myself
    - It's like a bookmark pointing to the last known commit on the master branch on origin![zz-remote-tracking-branch](../Assets/zz-remote-tracking-branch.png)

  - At the time you last communicated with this remote repository, here is where x branch was pointing
  - They follow this pattern `<remote>/<branch>`
    - `origin/master` references the state of the master branch on the remote repo named origin
    - `upstream/logoRedesign` references the state of the logoRedesign branch on the remote named upstream (a common remote name)
  - Run `git branch -r` to view the remote branches our local repository knows about
  - We can checkout these remote branch pointers using `git checkout origin/master`
    - To know what did this project look like when you first cloned this repo
    - This will put us in Detached HEAD

  

  ## Working with Remote Branch

  - Once You've cloned a repository , we have all the data and Git history for the project at that moment in time .However , that does not mean it's all in my workspace 
  - The github repo has a branch called puppies, but when I run `git branch` I don't see it on my machine! All I see is the master branch. What's going on?
    - Run `git branch -r` to view the remote branches our local repository **knows about**
  - When we clone some repo from Github, the local master branch is **automatically tracking** `origin/master`; however, other branches are not being tracked![z-local-remote-tracking-1](../Assets/z-local-remote-tracking-1.png)

  - We can use `git checkout origin/puppies`, but that results in detached HEAD state
  - Thus, I want my own **local branch** called puppies, and I want it to **be connected to `origin/puppies`**, just like my local master branch is connected to `origin/master`
  - We can run `git switch <remote-branch-name>` to **create a new local branch** from the remote branch of the same name AND sets it up to **track the remote branch** `origin/<remote-branch-name>`![z-local-remote-tracking-2](../Assets/z-local-remote-tracking-2.png)