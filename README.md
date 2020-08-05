# git-expand 
Expand git with a set of useful utilities and workflows

## To use:
Download or clone the repo and add the path to the bin folder to `PATH`. (Or copy its contents into a `PATH` folder)

## Commands
All commands are prefaced with git. e.g. `git root`
- [git root](#git_root)
- [git summary](#git_summary)
- [git-effort](#git_effort)
- [git-author](#git_author)

---

### git root
usage: `git root`

```
                Outputs the path to the root of the repo
```

### git summary
usage: `git summary [--line]`
```
                Outputs a summary of the repo by commits
    --line      Outputs a summary of the repo by line
```

|||
|---|---|
|Project|Project name|  
|Repo age|Age of the oldest commit|  
|Activity|Sum of unique hours with commits in|  
|Files|Total amount of files in the project|  
|Commits|Total amount of commits in a project|  
|Lines|Total amount of lines in a project|  
|Authors|Total lines/commits of the author, author name, percentage contribution|

Default summary
```
$ git summary
 Project    : CCRPG
 Repo age   : 5 years ago
 Activity   : 83 hours
 Files      : 63
 Commits    : 192
 Authors :
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
 Activity   : 83 hours
 Files      : 63
 Lines   : 4197
 Authors :
   3339 Alex           79.6%
    717 Adam           17.1%
     77 tvmanboy       1.8%
     50 Peguin666      1.2%
      9 Adam Hawley    0.2%
      5 Adam Plaskitt  0.1%
```

### git effort
usage: `git effort [-h] [--above <int>] [--author <name>]`
```
                Lists: files, commits to the files, active hours on file.
                Ordered by the target type: default commits
    -h          Changes target type to active hours
    --above <int>
                Only lists entires with target type above int
    --author <name>
                Only registory commits and active hours from the provided author
```

### git author
usage: `git author [--no-email]`
```
                Lists all authors and their email address that have contributed 
                to the project
    --no-email  Lists all authors connected to a project without their email
                address
```