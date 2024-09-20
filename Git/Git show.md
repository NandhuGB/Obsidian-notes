
git show helps to see the committed content in the repo.

```shell
git show
```

it returns the last commit and what changes where made

```shell
git show HEAD~[commit level, example:1,2,3,...]
```
we can give HEAD~1 to see second last commit.

```shell
git show [commit hash]
```

### ls-tree

ls-tree return the name of the files in the particular commit

```shell
git ls-tree HEAD
```

we can use commit / file (blob and tree) hash to look up as well.
```shell
git ls-tree d277fge
```