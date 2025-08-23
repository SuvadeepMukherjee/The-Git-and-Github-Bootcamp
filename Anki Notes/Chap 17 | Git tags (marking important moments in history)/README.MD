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
| Major release | No                      | Yes              | Complete revamp  | V2.0.0   |

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

#### Q10:How to create lightweight tags ? 

**Solution**:

- use `git tag tag-name` to create a lightweight tag 
- By default git will create the tag referring to the commit that HEAD is referring

#### Q11:How to create annotated tags ?

**Solution**:

- use `git tag -a` to create a new annotated tag 
- git will then open your default text editor and prompt you for additional information 

#### Q12:How to see the metadata of an annotated tag ? 

**Solution**;

To see the metadata of annotated tag, use `git show <tagname>`

#### Q13:How to tag a previous commit ? 

**Solution**:

We can also tag an older commit by providing the commit hash

`git tag -a tagname commit-hash`

#### Q14:Git will yell at us if we try to reuse a tag that is already referring to a commit . If we use the ____ option , we can FORCE our tag through and thus move the tag to the new commit we want to have that tag

**Solution**:

`git tag -f v1.0.0`

1. Git will yell at us if we try to **reuse a tag** that is already referring to a commit
2. If we use the `-f` option, we can FORCE our tag through and thus move the tag to the new commit we want to have that tag

##### Q15:How to delete a tag ? 

**Solution**:

Use `git tag -d tagname` to delete a tag 

#### Q16:By default does `git push` push tags to remote ? 

**Solution**:

- By default `git push` does not transfer tags to remote servers 

#### Q17:How to push all of your tags to the remote ? 

**Solution**:

- `git push <remote> --tags`

#### Q18:How to push a single tag to remote ? 

**Solution**:

`git push remote tag-name`

#### Q19:Practise exercise to practise git tags 

- Clone this [repo](https://github.com/tastejs/todomvc)
- Checkout on a new branch `tags-practise`

1. q1 : git command which will print a list of all the tags in the current repositiry 
2. Print a list of tags that include pre in their name 
3. View the state of the repo at the tag `v1.0`
4. Comapare tags 1.0 and 1.0.1 
5. Edit some files in the markdown and create a lightweight tag `v1.4.1`
6. Edit some more lines in the markdown and create an annotated tag `v1.4.2`
7. See the metadata of the tag `v1.4.2`
8. Give the commit hash `6b217afb` a tag `major` 
9. Add some more lines on README.MD add and commit then again give it a tag `v1.4.2` (it already exists)
10. Now delete the tag v`1.4.2`
11. Create a remote on origin lets call it `practise-tags` and then push only the `1.0` tag
12. Push all the tags to `practise-tags`



**Solution**:

1. git command which will print a list of all the tags in the current repository ➡️ `git tag`
2. We can search for tags that match a particular pattern by using `git tag -l <regex>`
   - For example `git tag -l "*pre*"` will print a list of tags that include "beta" in their name
3. To view the state of the repo at the tag `v1.0` do `git checkout v1.0`
4. To compare 2 tags use `git diff 1.0 1.0.1`
5. To create lightweight tags use `git tag tag-name` to create a lightweight tag , by default git will create the tag referring to the commit that HEAD is referring
6. use `git tag -a` to create a new annotated tag, git will then open your default text editor and prompt you for additional information
7. To see the metadata of the annotated tag v1.4.2 use the following command `git show v1.4.2`
8. git tag -a major `6b217afb`
9. Git will yell at us if we try to **reuse a tag** that is already referring to a commit . If we use the `-f` option, we can FORCE our tag through and thus move the tag to the new commit we want to have that tag . Command : `git tag -f v1.4.2`
10. Use `git tag -d tagname` to delete a tag , Command : `git tag -d v1.4.2`
11. `git push practise-tags 1.0`
12. `git push practise-tags --tags`
