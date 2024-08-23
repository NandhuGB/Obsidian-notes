
### Intialising git repo
```
git init
```


### Git repo status
```
git status
```

### Short status
```
git status -s
```

### Adding files to staging area
```
git add .  

git add <file names>
git add <shortcuts>
```

### Committing changes
```
git commit -m "commiting message"


git commit 
```

### Committing without staging area
```
git commit -am "commit  message"

git commit -a -m "commit message"
```

### Lisiting files in the staging area
```
git ls-files
```


### Removing files from staging area
```
git rm <file name / pattern>

```

### Renaming / moving files
```
git mv <current name> <new name>
```

### Ignoring files
```
# first create gitignore files

echo .gitignore

# add directories inside .gitignore file. so git ignore the unwanted files and directories


# gitignore.io website will help with predefined git ignore files for the our project

```

### Ignoring files from the commited repo

```
# if we want to ignore directories and files from the already commit repo, we have to add them into gitignore and remove it from the index (staging area).

# listing files in git index (staging area)
git ls-files 

# removing files from git index

git rm --cached <file-name>

git rm --cached -r <directories>
```

### Short Status

```
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

```
git restore --staged [file_name/ pattern/ .]
```

### Clearing unstaged working directory files

it restores the modified working directory files to previous commited version.

```
git restore [file_name/ pattern/ .]
```
