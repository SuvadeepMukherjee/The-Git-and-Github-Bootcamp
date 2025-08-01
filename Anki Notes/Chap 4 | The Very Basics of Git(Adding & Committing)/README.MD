## Chap 4 | The Very Basics of Git (Adding & Committing)

Anki Tag : 04-adding-and-committing

**Q1**: What is a git repo ? 

**Answer**:

- A git repo is a workspace which tracks and manages files within a folder
- We can have  as many repos on our machine as needed , all with seperate histories and contents 

![](../../Assets/git-repo.png)

**Q2**: How to check the status of a git repo ? 

**Answer**:

`git status` : gives information on the current status of a git repository and its contents 

**Q3**: How to initialize a new git repo ? 

**Answer**:

- `git init` ➡️ creates a new git repository 
- Do once per project , initialise the repo in the top-level folder containing our project 
- will create a hidden `.git` folder for us 

**Q4**: We have created a new git repo inside a git repo , how to fix it ? 

**Answer**:

- check all files with `ls -a` then delete the nested `.git` folder with `rm -rf`

**Q5:** What is Working Directory , Staging area and Repository ? 

**Answer**:

Working Directory ➡️ When we edit some files and check git status that is @ working directory 

Staging Area ➡️ We add files from the working directory to the staging area with `git add`

Repository ➡️ We move files from the the staging area to the Repository with `git commit`

![](../../Assets/committing-workflow.png) 

**Q6**: How to add all files and individual files from Working directory to staging area ? 

**Answer**:

add all files from working directory to staging area ➡️ `git add .`

add individual files from working directory to staging area with ➡️ `git add file1 file2`

**Q7**: How to see logs of all commits ? 

**Answer**:

To see logs of all commits use ➡️ `git log`

#### Q8:What is the command to commit files from the staging area to repository (inline commit message)

**Answer**:

`git commit  -m "message"`