## Chap 20 | Writing Custom Git Alias

## The Global Git Config File

- Git looks for the global config file at either `~/.gitconfig` or `~/.config/git/config`
- Any configuration variables that we change in the file will be applied across all Git repos
- We can also alter configuration variables from the command line if preferred

## Adding Aliases

- We can easily set up Git aliases to make our Git experience a bit simpler and faster
  - For example, we could define an alias ` git c` instead of having to type `git commit`
  - Or, we could define a custom `git l` command that prints out a custom formatted `commit log`
- Just add the below in your global `~/.gitconfig` file

```bash
[alias]  
s = status
l = log
cm = commit -m
```

- Or, configure alias from the command line using the "dot syntax"

```bash
git config --global alias.showMeBranches branch
```

## Existing Useful Alias

1. [Must Have Git Aliases: Advanced Examples](https://www.durdn.com/blog/2012/11/22/must-have-git-aliases-advanced-examples/)
2. [Thw Ultimate Git Alias Setup](https://gist.github.com/mwhite/6887990#the-ultimate-git-alias-setup)
3. https://github.com/GitAlias/gitalias