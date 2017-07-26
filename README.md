# Git-Settings

## log with filenames
``` git
git log --stat --oneline
```

## alias

### lg
```
git config --global alias.lg "log --graph --abbrev-commit --decorate --date=relative --pretty=format:'%C(dim yellow)%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'"
```

### s
```
git config --global alias.s "status -s"
```

