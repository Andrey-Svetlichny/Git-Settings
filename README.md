# Git-Settings

## log with filenames
``` git
git log --stat --oneline
```

## Alias

### lg
```
git config --global alias.lg "log --graph --decorate --pretty=format:'%C(yellow)%h%Creset %>(13)%ar %C(yellow)%d%Creset %s'"
```

### lg2
alternative (with author name, absolute date)
```
git config --global alias.lg2 "log --graph --decorate --pretty=format:'%C(yellow)%h%Creset%x09%>(13)%ad %C(green)%<(15,trunc)%an%Creset %C(yellow)%d%Creset %s' --date=format:'%y-%m-%d %H:%m'"
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
## Diff in Total Commander

Change button bar, add kdiff3

Parameters:
```
%X"%P%N" "%T%M"
```
or
```
%C1 %C2
```

## Useful commands 

### My commits with files \*ByCar\*.cs
```
git log --author="Svet" --stat --oneline *ByCar*.cs
```

### Who modified file?
```
git log --pretty=format:"%h %an" --stat *FactLoadByCar*.cs
```
 
### Show deleted file
```
git show a705c529 -- ELIS_Service/WebAPI/FactLoadByCarWebAPI.cs
```

### Checkout deleted file
```
git checkout a705c529 -- ELIS_Service/WebAPI/FactLoadByCarWebAPI.cs
```

### Compare current file version with old
```
git difftool fcdc2016 Head ELIS_Service/Services/FactLoadService.cs
```

### Log format
```
git log --pretty=format:"%C(yellow)%h%Creset %ad %C(green)%an" --date=format:"%y-%m-%d %H:%m" --stat *ByCar*.cs
```
