## Anki Notes 

#### Chap 3 | Installation & Setup (Anki Tag : 03-installation-and-setup)

**Q1**: Git command to set name and email ? 

**Answer**:

```bash
git config --global user.name "suvadeep"

git config --global user.email "suvadeepm0709@gmail.com"


```

**Q2**: Git command to check current  name and email ? 

**Answer**:

```bash
git config user.name

git config user.email
```

#### **Q3**: Terminal  commands  for the following 

1. list the contents of current working directory/ specified working directory
2. Open the current working directory , open a specified folder 
3. print working directory 
4. change directory 
5. move back one folder 
6. create a file called app.js
7. create a directory 
8. delete a file called hello.txt
9. delete a folder called LandTurtles 

**Answer**:

1. ls => list the contents of current working directory , ls folder => list the contents of a specified folder 
2. open . => open the current folder , `open <directory>` => open a specified folder 
3. pwd => print working directory 
4. `cd <dir>` => change directory to dir 
5. cd .. => move back one directory 
6. touch app.js
7. mkdir dir
8. `rm hello.txt`
9. `rm -rf LandTurtles`

------

### Chap 4 | The Very Basics of Git : Adding & Committing (anki tag : 04-adding-and-committing)

**Q1**: What is a git repo ? 

**Answer**:

- A git repo is a workspace which tracks and manages files within a folder
- We can have  as many repos on our machine as needed , all with seperate histories and contents 

![](../Assets/git-repo.png)

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

**Q4**: What is Working Directory , Staging area and Repository ? 

**Answer**:

Working Directory ➡️ When we edit some files and check git status that is @ working directory 

Staging Area ➡️ We add files from the working directory to the staging area with `git add`

Repository ➡️ We move files from the the staging area to the Repository with `git commit`

![](../Assets/committing-workflow.png) 

**Q5**: How to add all files and individual files from Working directory to staging area ? 

**Answer**:

add all files from working directory to staging area ➡️ `git add .`

add individual files from working directory to staging area with ➡️ `git add file1 file2`

**Q6**: How to see logs of all commits ? 

**Answer**:

To see logs of all commits use ➡️ `git log`

#### Q7:What is the command to add all modified files and commit in shortcut way ? 

**Answer**:

`git commit -a -m "message"`

------

## Chap 5 | Commits in details (05-commits-in-details)

#### Q1: How should commits be and how should commit messages be ? 

**Answer**:

- Commits should be atomic (keep each commit focussed on a single thing)
- Commit messages must be like "ordering the code base to change behavior"

#### Q2:How to write longer commit messages with git commit in Vim ? 

**Answer**:

1. i ➡️ insert mode 
2. Enter Commit Message 
3. ESC ➡️ Leave insert mode
4. :wq ⏎ ➡️ Leave insert mode 

✅ **I Eat Worms Quickly**
 → `i` → `ESC` → `:wq`
 → Insert → Escape → Save & Exit

#### Q3: We can write longer commit messages with git commit and then writing the commit message in vim , when writing the commit message we can use a concise one-sentence summary as the first sentence and then add a longer summaty if necessary .This way we can use _______ to display a concise git log 

**Answer**:

`git log --oneline`

#### Q4:Suppose we just made a commit and then realized we forgot to include a file! or maybe we made a typo in the commit message that we want to correct, Rather tham making a brand new seperate commit , we can redo the previous commit using ______

**Answer**:

```bash
git commit -m "Some Commit"

git add forgotten_file (Add to staging area)

git commit --amend
```

 Note ➡️ We have to write the new commit message in Vim

#### Q5:What is the command to exit git log and git log --oneline ? 

**Answer**:

- q 

##### Q6: We tell Git which files and directories to ignore in a given repository using a _____ file 

**Answer**: 

`.gitignore`
