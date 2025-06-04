# Git and GitHub Practice 🚀

This repo contains all my hands-on practice and notes while learning Git and GitHub following [this video tutorial](https://www.youtube.com/watch?v=zTjRZNkhiEU).

I’m posting all the commands, small learnings, and screenshots to show my understanding while doing it. (Very real, no fancy edits 😅)

---

## Git Init and Hidden Folders

```bash
(base) sanjanareddy@Gs-MacBook-Pro Git & Github % ls
(base) sanjanareddy@Gs-MacBook-Pro Git & Github % mkdir gitone gittwo gitthree
(base) sanjanareddy@Gs-MacBook-Pro Git & Github % ls
gitone          gitthree        gittwo
```

Some basic Linux commands revision:
- `ls` — to list files and folders
- `mkdir <folder>` — to create folders
- `cd ..` — to go back
- `pwd` — to check current working directory

---

These files are not automatically tracked by Git.  
I need a command to make sure Git tracks these.

➔ Important thing I learnt:  
> Git lets you **choose** which files/folders you want to track — it doesn't force you.  
> For example, I can track `gitone` and `gittwo`, but ignore `gitthree` if I want.

---

### Quick Recap

- **Git** = Software for version control.
- **GitHub** = Hosting service for Git repositories.
- **Git** helps track file changes and makes collaboration easy.

---

### Check Git Version

```bash
git --version
```

> I found it interesting that even when Git adds new features, they don’t break old ones — very stable software.

I had Git 2.15.0 initially.  
Updated it using Homebrew:
```bash
brew update
brew upgrade git
```

---

## What is a Repo?

A **repo** is basically a folder where your project files are kept along with Git tracking information.

---

## Git Status and Init

```bash
git status
git init
```

- `git init` — initializes Git tracking inside the folder (only needs to be done once per project).
- After `git init`, a hidden folder `.git` is created.

To see hidden files:
```bash
ls -la
```
📸 *(Screenshot here of `ls -la` showing `.git` folder)*

Inside `.git` folder:
```bash
cd .git
ls
```

> **Note**: `.git` folder has folders like `HEAD`, `config`, `hooks`, `objects`, `refs`.  
> **We should not touch or modify these manually** — Git handles it.

---

## Git Workflow Diagram

*(Add your image here)*

```markdown
![Git Workflow Diagram](./path-to-your-image.png)
```

### Quick Summary:
- `git add` ➔ moves changes to **Staging Area**.
- `git commit` ➔ saves them in the **Repo**.
- `git push` ➔ sends them to **GitHub**.

---

## Git Commit and Logs

Commands I used:
```bash
touch testone.txt testtwo.txt
git add testone.txt
git status
```
- `git add <file>` — adds specific file to staging.
- `git add .` — adds everything to staging.

*(Screenshot showing staged and unstaged files)*

To undo staging:
```bash
git reset HEAD <file>
```

To commit:
```bash
git commit -m "add file one"
```
*(Screenshot of commit message and Git Graph view)*

---

### What are Atomic Commits?

While reading about commits, I learnt about *Atomic Commits*:
- A commit should do **one logical thing only**.
- Should not mix unrelated changes.
- Keeps commit history clean and understandable.

---

### Commit Message Style Debate (Fun Fact)

I found there’s a debate:  
**Should commit messages be in past tense or present tense?**

Turns out, official Git guidelines recommend:  
**Present tense, imperative mood**.

Example:
- Good: `Add new login feature`
- Bad: `Added new login feature`

*(Honestly feels aggressive, but that’s the standard 😅)*

---

## Git Config: Username Setup

### Global Username (for all repos)

```bash
git config --global user.name "Your Name"
```

To confirm:
```bash
git config --global user.name
```

---

### Local Username (only for this repo)

```bash
git config user.name "Your Name"
```
To confirm:
```bash
git config user.name
```

*(Screenshots attached here for global and local username setups)*

---

## Git Logs

```bash
git log
git log --oneline
```

*(Screenshots of the commit log and oneline view)*

---

## Extra Things I Learnt

- There are so many `git log` options — filters by author, date, grep by message — looks very powerful.
- `git ls-files` — lists all files being tracked by Git (extra command I found useful).
- `git diff` — shows what changed but not yet staged.
- `git diff --staged` — shows what’s staged but not committed yet.

---

# 🌟 Still Continuing...

More notes and practice coming as I learn!  
I’ll update this README as I go along 🚀

---

### 📸 Screenshot Index

- `.git` hidden folder
- Inside `.git`
- Git Workflow Diagram
- Git Add and Commit (staged files)
- Git Graph view
- Git Log and Oneline
- Git Config Global/Local username

---

**💬 Side note:**  
If you’re reading this — don’t worry if you’re slow. Git takes a little time to get used to. Keep practicing small things every day.
