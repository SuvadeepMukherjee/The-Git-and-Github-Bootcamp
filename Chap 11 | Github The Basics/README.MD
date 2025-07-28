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