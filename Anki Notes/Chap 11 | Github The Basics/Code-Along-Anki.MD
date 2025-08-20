## Github - Basics Code Along Anki 

##  Code Along

#### Q1:Create a new git repo on your local and connect it to a new remote on Github(name the remote origin) 

#### Q2:Add another remote to the local(name it upstreams) and then view the remotes to verify both simply and with the verbose command

#### Q3:Rename the remote upstreams to upstream

#### Q4:Push your local code both to upstream and origin

#### Q3:Remove  the remote  upstream

**Solution**:

- git remote add origin URL 
- git remote add upstreams URL ,git remote , git remote -v
- git remote rename upstreams upstream
- git push origin master , git push upstream master
- git remote remove upstream



## Questions

#### Q1:What is a remote ? 

**Solution**:

- Before we can push anything on Github , we need to tell Git about our remote repository on Github
- We need to *setup a destination to push up to* 
- *In Git we refer to these destinations as remote .Each remote is simply a URL where a hosted repository lives*

#### Q2:What's the difference between main and master ?

**Solution**:

**The official name in git for the default branch is master while the official name of the default branch in Github is main

If you start your project from scratch by creating a repo on Github and clone it to your local machine the default branch will be main and need no further changes

However if you have your local repo with master as default branch and want to change that branch name correspond to Githubs standard use \*git branch -M main\***

 