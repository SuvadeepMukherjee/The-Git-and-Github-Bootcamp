# Chap 11 | Github : The Basics

## Introduction to Github 

- Github is a hosting platform for git repositories .You can put your own Git repos on Github and access them anywhere and share them with people around the world 

Git versus Github 

- Git 
  - version control software 
  - runs locally on your machine
  - dont need to register for an account 
  - dont need the internet to use it 

- Github 
  - a service that hosts Git repositories in the cloud
  - makes it easier to colloborate with other people 
  - need to sign up for an account 
  - an online place to share work that is done using git

## Cloning Github Repos with Git Clone 

- So far we have created our own Git repositories from scratch , but often we want to get a local copy of an existing repository instead 
- To do this , we can clone a remote repository hosted on Github or similar websites 
  - All we need is a URL that we can tell Git to clone 

To clone a repo simply run `git clone <url>`

-  Git will retreive all the files associated with the repository and will copy them to your local machine 
- In addition , Git initializes a new repositiory on your machine , giving you access to the full history of the cloned project ➡️ make sure you are not in a repo when you clone 
- Wherever you run git clone , that is the place where git is going to create a new folder for you 

Note ➡️ `git clone <url>` will clone any hosted repo not just hosted on Github

## SSH Config

SSH Keys

-  You need to be authenticated on Github to do certain operations like pushing up code from your local machine
- Your terminal will prompt you every single time for your Github email and password , unless you generate and configure an SSH key 
- Once configured , you can connect to Github without having to supply your username /password

## Create Github Repo

Option 1 | With Existing Repo

If you already have an existing repo locally that you want to get on Github 

1. Create a new repo on Github 
2. Connect Your local repo(add a remote)
   1. Before we can push anything up on Github , we need to tell Git about our remote repository on Github
   2. We need to setup a destination to push up to 
   3. In Git we refer to these destinations as remote .Each remote is simply a URL where a hosted repository lives 
   4. `git remote add <name> <URL>`
3. Push up your changes to Github `git push -u origin main`

Option 2 | Start from scratch

If you havent begun work on your local repo 

- Create a brand new repo on Github 
- Clone it on your machine (`git clone <URL>`)
  - The local repo is automatically connected to Github
- Do some work locally 
- Push up your changes to Github

## Git Remote 

Viewing remotes 

- To view any existing remotes for your repository we can run `git remote` or `git remote -v` (verbose for more info)
- This just displays a list of remotes .If you havent added any remotes yet , you wont see anything![zzz-remote](../Assets/zzz-remote.png)

Adding a new remote 

- A remote is really 2 things : a URL and a label 
- To add a new remote , we need to provide both to Git 
- `git remote add <name>  <URL>`
- For example `git remote add origin https://github.com/SuvadeepMukherjee/Anki-Old-Decks`

**Origin**?

- This tells git, anytime I use the name "origin", I'm **referring** to this particular Github repo URL
- Origin is a **conventional Git remote name**, but it is not at all special. It's just a name for a URL
- When we clone a Github repo, the default remote name setup for us is called origin. You can change it. Most people leave it

Other commands

- `git remote rename <old> <new>`
- `git remote remove <name>`

## Git Push

1. Now that we have a remote set up, let's push some work up to Github using `git push <remote> <branch>`

2. We need to specify the **remote** we want to push up to AND the **specific local branch** we want to push up to that remote

3. For example, `git push origin master` tells git to push up the master branch to our origin remote

4. Push in detail

   - While we often want to push a local branch up to a remote branch of the same name, we don't have to
   - We can use `git push <remote> <local-branch>:<remote-branch>` to push a local branch up to a remote branch of **different name**
   - For example, `git push origin pancake:waffle` pushed our local pancake branch up to a remote branch called waffle

5. The `-u` option

   - The `-u` option allows us to set the **upstream** of the branch we're pushing
   - We can think of this as a **link** connecting our local branch to a branch on Github
   - `git push -u origin master` sets the upstream of the local master branch so that it **tracks the master branch on the origin repo**
   - Once we've set the upstream of a branch, we can use `git push` shorthand which will push our current branch to the upstream

   ```bash
   # without upstream, every time git push origin master
   # with upstream, first time git push -u origin master 
   # next time git push
   ```

   ## Main & Master: Github Default Branch

   1. [Why GitHub renamed its master branch to main](https://www.theserverside.com/feature/Why-GitHub-renamed-its-master-branch-to-main)
   2. If you start your project from scratch by creating a repo on Github and clone it to your local machine, the default branch will be `main` and need no further changes
   3. However, if you have your local repo with `master` as default branch, and want to change that branch name corresponds to Github's standard
      - Use `git branch -M main`