# Git-Settings

## log with filenames
``` git
git log --stat --oneline
```

## Alias

### lg
```
git config --global alias.lg "log --graph --abbrev-commit --decorate --date=relative --pretty=format:'%C(dim yellow)%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'"
```

### s
```
git config --global alias.s "status -s"
```
## Merge

```
git config --global --add diff.guitool kdiff3
git config --global --add merge.tool kdiff3
```

or

```
git config --global merge.tool meld
```
