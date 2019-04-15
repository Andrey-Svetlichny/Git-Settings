# Git-Settings

## git-diff to ignore ^M
git config --global core.whitespace cr-at-eol

## Russian characters 
### filenames
git config --global core.quotepath false

### gitk
git config --global gui.encoding utf-8

## Alias

### lg
```
git config --global alias.lg "log --graph --decorate --pretty=format:'%C(yellow)%h%Creset%x09%>(13)%ad %C(green)%<(15,trunc)%an%Creset %C(yellow)%d%Creset %s' --date=format:'%y-%m-%d %H:%m'"
```

### lg2
alternative (without author name, relative date)
```
git config --global alias.lg2 "log --graph --decorate --pretty=format:'%C(yellow)%h%Creset %>(13)%ar %C(yellow)%d%Creset %s'"
```

### s
```
git config --global alias.s "status -s"
```
## Merge

```
git config --global --add difftool.kdiff3.path "C:/Program Files/KDiff3/kdiff3.exe"
git config --global difftool.prompt false

git config --global --add mergetool.kdiff3.path "C:/Program Files/KDiff3/kdiff3.exe"
git config --global mergetool.keepBackup false
```

or

```
git config --global merge.tool meld
```
## Diff in Total Commander

Change button bar, add kdiff3

Parameters:
```
%C1 %C2
```

## Notepad++ from command line
add file c:\Users\Andrey\.bash_profile
```
function npp {
    "C:\Program Files (x86)\Notepad++\notepad++.exe" -multiInst -notabbar -nosession -noPlugin "$*";
}
export -f npp;
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

### Rewrite history
```
git log --pretty=format:'%C(yellow)%h%Creset%  %ad %cd%Creset %C(yellow)%d%Creset %s' --date=format:'%y-%m-%d %H:%m'
git rebase -i --root
git filter-branch --env-filter 'GIT_COMMITTER_DATE=$GIT_AUTHOR_DATE; export GIT_COMMITTER_DATE'

git reflog expire --all --expire=now
git gc --prune=now --aggressive
```
