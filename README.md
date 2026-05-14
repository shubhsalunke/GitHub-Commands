# GitHub Commands

# Prerequisites

* Git installed on system
* GitHub account
* Internet connection

---

# 1. Check Git Installation

```bash
git --version
```

---

# 2. Configure Git

Set username:

```bash
git config --global user.name "Your Name"
```

Set email:

```bash
git config --global user.email "your-email@gmail.com"
```

Verify configuration:

```bash
git config --list
```

---

# 3. Create Project Folder

```bash
mkdir myproject
cd myproject
```

---

# 4. Initialize Git Repository

```bash
git init
```

---

# 5. Check Repository Status

```bash
git status
```

---

# 6. Create Files

```bash
touch app.py
```

OR

```bash
nano app.py
```

---

# 7. Add Files to Staging Area

Add single file:

```bash
git add app.py
```

Add all files:

```bash
git add .
```

---

# 8. Commit Changes

```bash
git commit -m "Initial commit"
```

---

# 9. Create GitHub Repository

Go to:

[GitHub](https://github.com?utm_source=chatgpt.com)

Create a new repository.

Example:

* Repository Name: `myproject`

---

# 10. Connect Local Repository to GitHub

```bash
git remote add origin https://github.com/username/myproject.git
```

Check remote:

```bash
git remote -v
```

---

# 11. Push Code to GitHub

Rename branch:

```bash
git branch -M main
```

Push code:

```bash
git push -u origin main
```

Future push commands:

```bash
git push
```

---

# 12. Clone Existing Repository

```bash
git clone https://github.com/username/repository-name.git
```

Example:

```bash
git clone https://github.com/eyeisr/ipp.git
```

---

# 13. Pull Latest Changes

```bash
git pull
```

---

# 14. View Commit History

```bash
git log
```

Short version:

```bash
git log --oneline
```

---

# 15. Branch Management

Create new branch:

```bash
git checkout -b dev
```

Switch branch:

```bash
git checkout main
```

Merge branch:

```bash
git merge dev
```

Delete branch:

```bash
git branch -d dev
```

---

# 16. Remove Files

```bash
git rm filename
```

Commit removal:

```bash
git commit -m "Removed file"
```

---

# 17. Undo Changes

Undo file changes:

```bash
git checkout -- filename
```

Remove staged changes:

```bash
git reset filename
```

---

# 18. Git Ignore

Create `.gitignore` file:

```bash
nano .gitignore
```

Example:

```text
node_modules/
.env
__pycache__/
```

---

# 19. Complete GitHub Workflow

```bash
cd project-folder

git init

git add .

git commit -m "First commit"

git branch -M main

git remote add origin https://github.com/username/repo.git

git push -u origin main
```

---

# 20. Daily Workflow Commands

Check status:

```bash
git status
```

Add changes:

```bash
git add .
```

Commit changes:

```bash
git commit -m "Updated project"
```

Push code:

```bash
git push
```

Pull latest updates:

```bash
git pull
```

---

# 21. SSH Setup for GitHub

Generate SSH key:

```bash
ssh-keygen -t ed25519 -C "your-email@gmail.com"
```

Start SSH agent:

```bash
eval "$(ssh-agent -s)"
```

Add SSH key:

```bash
ssh-add ~/.ssh/id_ed25519
```

Show public key:

```bash
cat ~/.ssh/id_ed25519.pub
```

Add SSH key here:

[GitHub SSH Settings](https://github.com/settings/keys?utm_source=chatgpt.com)

Test SSH connection:

```bash
ssh -T git@github.com
```

Clone repository using SSH:

```bash
git clone git@github.com:username/repo.git
```

---

# 22. Common Git Errors

## Permission Denied

```bash
ssh -T git@github.com
```

---

## Repository Not Found

Check:

* Repository name
* GitHub username
* Access permissions

---

## Push Rejected

Pull latest changes first:

```bash
git pull origin main --rebase
```

Then push again:

```bash
git push
```

---

# 23. Best Practices

* Use meaningful commit messages
* Push code regularly
* Use `.gitignore`
* Create separate branches for features
* Never upload passwords or secrets
* Always check `git status`
