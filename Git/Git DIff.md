 
git diff helps to compare the changes between staged and working directory, commited and stages directories.

```shell
git diff 
```

![]()![[Screenshot from 2022-12-08 15-29-34.png]]

1. first row represents the files that compared
2. meta data from staging area
3. this is commited file 
4. this is working directory
5. -43,5 line changed to --> +43,5 means no line added but changes in the 43 line at 5th index
6. that is previous line to the changed line
7. code in commited directory
8. code in the working directory


```shell
git diff --staged

```

it will give same output but by comparing staged code and commited code.

there is different GUI tools available to see these changes more organised. this will be helpful when youare working the big repo with last of changes.


