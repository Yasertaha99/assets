# **comprehensive Git cheat sheet** covering all the Git commands you may need in **real-world development**, including **common, intermediate, and advanced commands**. I’ll also include explanations and examples so it’s ready for quick reference.

Here’s a full cheat sheet:

---

# 📝 Git Cheat Sheet for Development

---

## 1️⃣ **Setup & Config**

| Command                                              | Description           | Example                                             |
| ---------------------------------------------------- | --------------------- | --------------------------------------------------- |
| `git config --global user.name "Name"`               | Set global username   | `git config --global user.name "John Doe"`          |
| `git config --global user.email "email@example.com"` | Set global email      | `git config --global user.email "john@example.com"` |
| `git config --list`                                  | Show config           | `git config --list`                                 |
| `git init`                                           | Initialize a new repo | `git init my-project`                               |
| `git clone <url>`                                    | Clone remote repo     | `git clone https://github.com/user/repo.git`        |

---

## 2️⃣ **Basic Workflow**

| Command                    | Description                  | Example                                   |
| -------------------------- | ---------------------------- | ----------------------------------------- |
| `git status`               | Show current changes         | `git status`                              |
| `git add <file>`           | Stage file(s)                | `git add app.vue`                         |
| `git add .`                | Stage all changes            | `git add .`                               |
| `git commit -m "message"`  | Commit staged changes        | `git commit -m "feat: add login feature"` |
| `git commit -am "message"` | Stage + commit tracked files | `git commit -am "fix: typo in README"`    |
| `git log`                  | Show commit history          | `git log --oneline --graph --all`         |

---

## 3️⃣ **Branching**

| Command                    | Description                 | Example                         |
| -------------------------- | --------------------------- | ------------------------------- |
| `git branch`               | List branches               | `git branch`                    |
| `git branch <name>`        | Create a branch             | `git branch feature/login`      |
| `git checkout <branch>`    | Switch branch               | `git checkout develop`          |
| `git switch <branch>`      | Modern way to switch branch | `git switch feature/login`      |
| `git checkout -b <branch>` | Create + switch             | `git checkout -b feature/login` |
| `git merge <branch>`       | Merge branch into current   | `git merge develop`             |
| `git branch -d <branch>`   | Delete branch               | `git branch -d feature/login`   |

---

## 4️⃣ **Remote Repositories**

| Command                       | Description                 | Example                                                  |
| ----------------------------- | --------------------------- | -------------------------------------------------------- |
| `git remote -v`               | Show remotes                | `git remote -v`                                          |
| `git remote add origin <url>` | Add remote repo             | `git remote add origin https://github.com/user/repo.git` |
| `git push`                    | Push commits to remote      | `git push origin main`                                   |
| `git push -u origin <branch>` | Push new branch             | `git push -u origin feature/login`                       |
| `git pull`                    | Fetch + merge changes       | `git pull origin main`                                   |
| `git fetch`                   | Fetch updates without merge | `git fetch origin`                                       |

---

## 5️⃣ **Undo / Reset / Revert**

| Command                       | Description                    | Example                        |
| ----------------------------- | ------------------------------ | ------------------------------ |
| `git restore <file>`          | Discard changes in working dir | `git restore app.vue`          |
| `git restore --staged <file>` | Unstage a file                 | `git restore --staged app.vue` |
| `git reset HEAD <file>`       | Unstage file (older style)     | `git reset HEAD app.vue`       |
| `git reset --soft <commit>`   | Move HEAD, keep changes staged | `git reset --soft HEAD~1`      |
| `git reset --mixed <commit>`  | Move HEAD, unstage changes     | `git reset --mixed HEAD~1`     |
| `git reset --hard <commit>`   | Reset HEAD & working dir       | `git reset --hard HEAD~1`      |
| `git revert <commit>`         | Create new commit to undo      | `git revert 9a0b1f2`           |

---

## 6️⃣ **Stashing**

| Command           | Description              | Example                    |
| ----------------- | ------------------------ | -------------------------- |
| `git stash`       | Save uncommitted changes | `git stash`                |
| `git stash list`  | Show stashes             | `git stash list`           |
| `git stash apply` | Reapply last stash       | `git stash apply`          |
| `git stash pop`   | Apply + remove stash     | `git stash pop`            |
| `git stash drop`  | Delete a stash           | `git stash drop stash@{0}` |

---

## 7️⃣ **Viewing / Comparing**

| Command                            | Description           | Example                            |
| ---------------------------------- | --------------------- | ---------------------------------- |
| `git log`                          | Commit history        | `git log --oneline`                |
| `git log --graph --decorate --all` | Visual commit graph   | `git log --graph --decorate --all` |
| `git diff`                         | Show unstaged changes | `git diff`                         |
| `git diff --staged`                | Show staged changes   | `git diff --staged`                |
| `git show <commit>`                | Show commit details   | `git show 9a0b1f2`                 |

---

## 8️⃣ **Tagging / Releases**

| Command                          | Description   | Example                             |
| -------------------------------- | ------------- | ----------------------------------- |
| `git tag`                        | List tags     | `git tag`                           |
| `git tag <name>`                 | Create tag    | `git tag v1.0`                      |
| `git tag -a <name> -m "message"` | Annotated tag | `git tag -a v1.0 -m "Release v1.0"` |
| `git push origin <tag>`          | Push tag      | `git push origin v1.0`              |
| `git push origin --tags`         | Push all tags | `git push origin --tags`            |

---

## 9️⃣ **Rebasing**

| Command                  | Description                         | Example                 |
| ------------------------ | ----------------------------------- | ----------------------- |
| `git rebase <branch>`    | Reapply commits onto another branch | `git rebase main`       |
| `git rebase -i <commit>` | Interactive rebase                  | `git rebase -i HEAD~3`  |
| `git rebase --abort`     | Cancel rebase                       | `git rebase --abort`    |
| `git rebase --continue`  | Continue rebase after conflict      | `git rebase --continue` |

---

## 🔟 **Advanced / Helpful Commands**

| Command                    | Description                        | Example                   |
| -------------------------- | ---------------------------------- | ------------------------- |
| `git cherry-pick <commit>` | Apply specific commit              | `git cherry-pick 9a0b1f2` |
| `git blame <file>`         | Show line authors                  | `git blame App.vue`       |
| `git bisect start`         | Start binary search for bug        | `git bisect start`        |
| `git bisect good <commit>` | Mark good commit                   | `git bisect good HEAD~10` |
| `git bisect bad <commit>`  | Mark bad commit                    | `git bisect bad HEAD`     |
| `git reflog`               | View history of HEAD moves         | `git reflog`              |
| `git clean -fd`            | Remove untracked files/directories | `git clean -fd`           |

---

## 1️⃣1️⃣ **Git Aliases** (Optional, super handy)

```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.lg "log --oneline --graph --all --decorate"
```

---

## ⚡ Tips for Daily Development

1. Always `git pull --rebase` before starting new work
2. Commit **small, logical changes**
3. Use **feature branches** for new work
4. Keep `main` / `develop` branch stable
5. Use **descriptive commit messages**
6. Stash changes if switching branches quickly
7. Tag releases consistently


