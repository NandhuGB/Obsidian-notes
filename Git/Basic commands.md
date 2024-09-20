
### Intialising git repo
```shell
git init
```


### Git repo status
```shell
git status
```

### Short status
```shell
git status -s
```

### Adding files to staging area
```shell
git add .  

git add <file names>
git add <shortcuts>
```

### Committing changes
```shell
git commit -m "commiting message"


git commit 
```

### Committing without staging area
```shell
git commit -am "commit  message"

git commit -a -m "commit message"
```

### Lisiting files in the staging area
```shell
git ls-files
```


### Removing files from staging area
```shell
git rm <file name / pattern>

```

### Renaming / moving files
```shell
git mv <current name> <new name>
```

### Ignoring files
```shell
# first create gitignore files

echo .gitignore

# add directories inside .gitignore file. so git ignore the unwanted files and directories


# gitignore.io website will help with predefined git ignore files for the our project

```

### Ignoring files from the commited repo

```shell
# if we want to ignore directories and files from the already commit repo, we have to add them into gitignore and remove it from the index (staging area).

# listing files in git index (staging area)
git ls-files 

# removing files from git index

git rm --cached <file-name>

git rm --cached -r <directories>
```

### Short Status

```shell
git status -s

# it will gives you small brief status of the files

# from left to right, first column represents the staging area, second column 
represents the working directory.

# ?? means not yet tracked
# M means modified
# A means added to staging area
# M in green color means modified in staging area
# M in red means modified in working directory

```

### Unstaging files

it helps to remove unwanted staged files from staging area.

```shell
git restore --staged [file_name/ pattern/ .]
```

### Clearing unstaged working directory files

it restores the modified working directory files to previous commited version.

```shell
git restore [file_name/ pattern/ .]
```
