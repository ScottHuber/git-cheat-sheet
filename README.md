git-cheat-sheet
===============


diff current working file against file in another branch
```git difftool 9884f585ae0b7916fb87c7812aefbbf650ac4896 -- application/models/report_v2_model.php```

list local/remote branches and sort by date
```
alias listlocalbranches='for k in `git branch | perl -pe s/^..//`; do echo -e `git show --pretty=format:"%Cgreen%ci %Cblue%cr%Creset" $k -- | head -n 1`\\t$k; done | sort'
alias listlocalbranchesr='for k in `git branch | perl -pe s/^..//`; do echo -e `git show --pretty=format:"%Cgreen%ci %Cblue%cr%Creset" $k -- | head -n 1`\\t$k; done | sort -r' 
alias listremotebranches='for k in `git branch -r | perl -pe '"'"'s/^..(.*?)( ->.*)?$/\1/'"'"'`; do echo -e `git show --pretty=format:"%Cgreen%ci %Cblue%cr%Creset" $k -- | head -n 1`\\t$k; done | sort'
alias listremotebranchesr='for k in `git branch -r | perl -pe '"'"'s/^..(.*?)( ->.*)?$/\1/'"'"'`; do echo -e `git show --pretty=format:"%Cgreen%ci %Cblue%cr%Creset" $k -- | head -n 1`\\t$k; done | sort -r' 
```
