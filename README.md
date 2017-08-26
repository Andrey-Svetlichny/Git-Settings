# Git-Settings

## log with filenames
``` git
git log --stat --oneline
```

## Alias

### lg
```
git config --global alias.lg "log --graph --decorate --pretty=format:'%C(yellow)%h%Creset %>(13)%cr %C(green)%<(15,trunc)%an%Creset %C(yellow)%d%Creset %s'"
```

### s
```
git config --global alias.s "status -s"
```
## Merge

```
git config --global --add diff.guitool kdiff3
git config --global difftool.prompt false

git config --global --add merge.tool kdiff3
```

or

```
git config --global merge.tool meld
```
