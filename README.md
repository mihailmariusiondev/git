- Add & commit in one command

```
git config --global alias.ac '!git add -A && git commit'
git ac -m "my_commit_message"
```

- 🔴 Revert last 2 commits from master (**OJO elimina archivos locales**)

```
git reset --hard HEAD~2
git push -f
```

- 🟢 Revert last 2 commits from master (**mantiene archivos locales**)

```
git reset --soft HEAD~2
git push -f
```

- 🟢 Revert to specific commit id from master (**mantiene archivos locales**)

```
git reset --soft 9e494633c3744d42c1f6c549be8e451ff658bbb7
```

- 🔴 Discard local changes to all files (**OJO elimina archivos locales**):

```
git reset --hard
```

- 🟢 Git set new origin (migrations from github > bitbucket etc)

```
# View existing remotes
git remote -v

# Change the 'origin' remote's URL
git remote set-url origin <url>

# Verify new remote URL
git remote -v
```

