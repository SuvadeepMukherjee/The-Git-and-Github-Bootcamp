# Chap 17 | Git Tags - marking important moments in history 

Anki ➡️17-git-tags

#### Q1:What is a git tag ? 

**Solution**:

- pointers that refer to particular points in git history 
- Think of tags as branch reference that DO NOT CHANGE (Once a tag is created , it always refers to the same commit , its just a label for a commit)![01-git-tags](../../Assets/17-git-tags/01-git-tags.png)

#### Q2:Types of git tags

**Solution**:

**lightweight tags**: just a name/label to a particular commit

**annotated tags(preferred)**: store extra meta data including the authors name and email , the date and a tagging message

#### Q3:Versioning symbols 

**Solution**:

![02-semantic-versioning](../../Assets/17-git-tags/02-semantic-versioning.png) 

#### Q4:What is typically the initial release ? 

**Solution**:

Typically the initial release is `v1.0.0`

#### Q5:Major differences between patch release , minor release and major release 

|               | Backwards Compatibility | Breaking Changes | Purpose          | Examples |
| ------------- | ----------------------- | ---------------- | ---------------- | -------- |
| Patch Release | Yes                     | No               | bug fixes        | V1.0.1   |
| Minor Release | Yes                     | No               | add new features | V1.1.0   |
| Major release | No                      | Yes              | Compete revamp   | V2.0.0   |

#### Q6:Which git command will print a list of all the tags in the current repository ? 

**Solution**:

`git tag` ➡️ will print a list of all the tags in the current repository 

#### Q7:Print a list of tags that include beta in their name ? 

**Solution**:

- We can search for tags that match a particular pattern by using `git tag -l <regex>` 
  - For example `git tag -l "*beta*"` will print a list of tags that include "beta" in their name

#### Q8:To view the state of a repo at a particular tag we can use ___________

**Solution**:

To view the state of a repo at a particular tag we can use `git checkout <tag>` 

#### Q9:How to compare  2 tags 

**Solution**:

- To comapare 2 tags use `git diff v1.0.0 v2.0.0`
