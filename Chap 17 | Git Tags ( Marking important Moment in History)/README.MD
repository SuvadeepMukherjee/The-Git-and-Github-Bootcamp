# Chap 17 | Git Tags : Marking Important Moment in History



## Idea Behind Git Tags

- Tags are **pointers** that refer to particular points in Git history. We can mark a particular moment in time with a tag
- Tags are most often used to **mark version releases** in projects (v4.1.0, v4.1.1, etc.)![01-git-tags](./..//Assets/17-git-tags/01-git-tags.png)

- Think of tags as branch references that do NOT CHANGE.
  - Once a tag is created, it always refers to the same commit. It's just a **label for a commit**

- There are two types of Git tags we can use
  - **Lightweight tags**: just a name/label that points to a particular commit
  - **Annotated tags (preferred)**: store **extra meta data** including the author's name and email, the date, and a tagging message

## Semantic Versioning 

- The semantic versioning spec outlines a standardized versioning system for software releases
- It provides a consistent way for developers to give meaning to their software releases (how big of a change is this release?)
- Versions consist of **three numbers** separated by periods![02-semantic-versioning](./../Assets/17-git-tags/02-semantic-versioning.png)

- Initial Release: Typically, the initial release is v1.0.0
- **Patch Release** v1.0.1 v1.0.2
  - Normally do not contain new features or significant changes
  - typically signify bug fixes and other changes that **do not impact how the code is used**

- **Minor Release** v1.1.0
  - Signify that new features or functionality have been added
  - But the project is still **backwards compatible**
  - No breaking changes
  - The new functionality is optional and should not force users to rewrite their own code
- **Major Release** v2.0.0
  - Signify significant changes that is **no longer backwards compatible**
  - Features may be removed or changed substantially

## View and Search Tags

- `git tag` will print a list of all the tags in the current repository

- We can search for tags that match a particular pattern by using `git tag -l <regex>`

  - For example `git tag -l "*beta*"` will print a list of tags that include beta in their name

  

## Comparing Tags with Git Diff

1. To view the state of a repo at a particular tag, we can use `git checkout <tag>`
   - This puts us in detached HEAD!
2. Use `git diff v1.0.0 v2.0.0` to compare them for example


## Creating Lightweight Tags

1. Use `git tag <tagname>` to create a lightweight tag
2. By default, Git will create the tag referring to the **commit** that **HEAD is referencing**

## Creating Annotated Tags

1. Use `git tag -a` to create a new annotated tag
   - Git will then open your default text editor and prompt you for additional information
2. Similar to git commit, we can also use the `-m` option to pass a message directly and forgo the opening of the text editor
3. To see the metadata of annotated tag, use `git show <tagname>`

## Tagging Previous Commits

1. We can also tag an older commit by providing the commit hash: `git tag -a <tagname> <commit-hash>`

## Replacing Tag with Force

1. Git will yell at us if we try to **reuse a tag** that is already referring to a commit
2. If we use the `-f` option, we can FORCE our tag through and thus move the tag to the new commit we want to have that tag

Command : `git tag -f v1.0.0`

## Deleting Tag

1. Use `git tag -d <tagname>` to delete a tag

## Pushing Tags

1. By default, the `git push` command **DOES NOT** transfer tags to remote servers
2. If you have a lot of tags that you want to push up at once, you can use the `git push <remote> --tags`
   - This will transfer all of your tags to the remote server that are not already there
3. If you just want to push a single tag to remote, use `git push <remote> <tagname>`