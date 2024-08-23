
git show helps to see the committed content in the repo.

```
git show
```

it returns the last commit and what changes where made

```
git show HEAD~[commit level, example:1,2,3,...]
```
we can give HEAD~1 to see second last commit.

```
git show [commit hash]
```

### ls-tree

ls-tree return the name of the files in the particular commit

```
git ls-tree HEAD
```

we can use commit / file (blob and tree) hash to look up as well.
```
git ls-tree d277fge
```