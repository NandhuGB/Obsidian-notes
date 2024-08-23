
three layers of configurations
1. system - applies to all repo of every user in that system
2. global -  applies to all repo of the current user
3. local -  aplies to the current repo

## Git global Configuration

user name
```
git config --global user.name "Nandhagopal"
``` 

user email

```
git config --global user.email nandhagopal.b@yahoo.com
```

Changing core editor

```
git config --global  core.editor "code --wait"
```

editing configuration file using default editor

```
git config --global -e
```

****

### Configuring **core.autocrlf** settings
		windows systems ends the line with **/r/n**. linux and MacOs ends the line with **/n**. 
	/r - carriage return 
	/n - line feed

	to avoid problems raising with /r/n or /n. we have to configure the core .autocrlf settings for 
windows

```
git config --global core.aurocrlf true
```

linux / MacOs

```
git config --global core.autocrlf input
```


changing default branch name:

```
> git config --global init.defaultBranch <name>
```

Git difftool

```
git config --global diff.tool <-vscode->

git config --global difftool.vscode.cmd 'code --wait --diff $LOCAL $REMOTE'
```
	please verify the config by 'git config --global -e'