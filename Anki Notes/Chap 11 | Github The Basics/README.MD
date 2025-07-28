# Chap 11 | Github : The basics

Anki ➡️ 11-Github-The-basics

#### Q1:How to clone a public Github Repo ? 

**Answer**:

To clone a repo simply run `git clone <url>`

- Git will retreive all the files associated with the repository and will copy them to your local machine
- In addition ,Git initialises a new repository on your machine , giving you access to the full history of the cloned project ➡️make sure you are not in a repo when you clone
- Wherever you run git clone , that is the place where git is going to create a new folder for us

Note ➡️ `git clone <url>` will clone any hosted repo not just hosted on GitHub

#### Q2:What is a remote ? 

**Answer**:

- Before we can push anything up on Github , we need to tell Git about our remote repository on Github
- We need to setup a destination to push up to
- In Git we refer to these destinations as remote .Each remote is simply a URL where a hosted repository lives 

#### Q3:You already have an existing repo locally that you want to get on Github .What are the steps ?

**Answer**:

- Create a new repo on Github 
- Connect your local repo(add a remote)
  - `git remote add <name> <URL>`
- Push up your changes to Github

#### Q4:Create a github repo (you havent begun work on your local repo)

**Answer**:

- Create a brand new repo on Githhub
- Clone it on your machine (`git clone <URL>` , The local repo is automatically connected to Github)
- Do some work locally 
- Push up your changes to Github