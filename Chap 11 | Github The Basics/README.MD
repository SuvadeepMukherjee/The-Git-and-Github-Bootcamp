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

