# Useful GIT commands

---

## Get your local Git repository on <srouce version control provider>


```bash
# Step 1: Switch to your repository's directory
cd /path/to/your/repo

# Step 2: Connect your existing repository to Bitbucket

git remote add origin https://mariusmihailion@bitbucket.org/mariusmihailion/<repositoryName>.git
git push -u origin master

```


---

- Add & commit in one command

```
git config --global alias.ac '!git add -A && git commit'

# Usage:
git ac -m "my_commit_message"
```

- 🔴 Revert last 2 commits from master (**WARNING deletes local files**)

```
git reset --hard HEAD~2
git push -f
```

- 🟢 Revert last 2 commits from master (**keeps local files**)

```
git reset --soft HEAD~2
git push -f
```

- 🟢 Revert to specific commit id from master (**keeps local files**)

```
git reset --soft 9e494633c3744d42c1f6c549be8e451ff658bbb7
```

- 🔴 Discard local changes to all files (**WARNING deletes local files**):

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

