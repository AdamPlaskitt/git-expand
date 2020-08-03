# git-expand 
Expand git with a set of useful utilities and workflows

## To use:
Download or clone the repo and add the path to the bin folder to `PATH`. (Or copy its contents into a `PATH` folder)

## Commands
All commands are prefaced with git. e.g. `git root`
- [git root](#git_root)
- [git summary](#git_summary)

---

### git root
usage: `git root`

Outputs the path to the root of the repo

### git summary
usage: `git summary [--line]`
```
                Outputs a summary of the repo by commits
    --line      Outputs a summary of the repo by line
```
Default summary
```
$ git summary
 Project    : CCRPG
 Repo age   : 5 years ago
 active days: 46
 files      : 63
 Commits    : 192
 authors :
   143  Alex                 74.5%
    23  Adam                 12.0%
    12  tvmanboy             6.2%
     7  Peguin666            3.6%
     5  Adam Plaskitt        2.6%
     1  Adam Hawley          0.5%
     1  TheGuyOnHisComputer  0.5%
```

Summary by line
```
$ git summary --line
 Project    : CCRPG
 Repo age   : 5 years ago
 active days: 46
 files      : 63
 lines   : 4197
 authors :
   3339 Alex           79.6%
    717 Adam           17.1%
     77 tvmanboy       1.8%
     50 Peguin666      1.2%
      9 Adam Hawley    0.2%
      5 Adam Plaskitt  0.1%
```