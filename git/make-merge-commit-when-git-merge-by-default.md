# Make merge commit when git merge by default

To avoid fast-forward merge and make merge commit when `git merge`:


```
$ git merge --no-ff branch-to-be-merged
```

To do this by default:

```
$ git config --global --add merge.ff false
$ git config --global --add pull.ff only
```

(Second command will disable making merge commit when `git pull`.)
