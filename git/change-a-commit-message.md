# Change a commit message

At first display the commit log to check what number is the commit to be changed from HEAD:

```
$ git log --oneline
```

Then use the following command with replacing `n` with the number to display a list of commits in a editor:

```
$ git rebase -i HEAD~n
```

For example if the commit is 3rd, use `git rebase -i HEAD~3` . HEAD is the 1st.

If the commit to be changed is the first commit (=root commit), use the following command instead:

```
$ git rebase -i --root
```

In the displayed list rewrite `pick` at the beginning of the commit to `edit` and save it.
For example:

from

```
pick c8bc103 message
pick 8bb5df1 message
pick ec4002a message to change
.
.
.
```

to

```
pick c8bc103 message
pick 8bb5df1 message
edit ec4002a message to change
.
.
.
```

Then use following 2 commands to update the commit message:

```
$ git commit --amend -m "new message"
$ git rebase --continue
```

Finally force-push the commit:

```
$ git push -f
```

(Using `--force-with-lease` option instead is better)

---

If you want to rewrite the most recent commit message and the commit has not pushed:

```
$ git commit --amend -m "new message"
```
