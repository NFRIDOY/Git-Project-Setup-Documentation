# Git Project Setup Documentation

## Local Git Setup
### Configure Git Identity for the Current Project
```bash
git config --local user.name "username"
git config --local user.email "user@email.com"
```

## Global Git Setup
### Configure Git Identity Globally for All Projects
```bash
git config --global user.name "username"
git config --global user.email "user@email.com"
```

---

## Add Files and Push to Repository
**Using SSH or HTTPS (SSH recommended)**
## HTTPS

### Create a New Repository
1. Clone the repository:
   ```bash
   git clone https://gitlab.com/username/project_slug.git
   ```
2. Navigate to the repository:
   ```bash
   cd project_slug
   ```
3. Create and switch to the main branch:
   ```bash
   git switch --create main
   ```
4. Add a README file:
   ```bash
   touch README.md
   git add README.md
   git commit -m "add README"
   git push --set-upstream origin main
   ```

### Push an Existing Folder to the Repository
1. Navigate to your folder:
   ```bash
   cd existing_folder
   ```
2. Initialize the Git repository:
   ```bash
   git init --initial-branch=main
   ```
3. Add the remote origin:
   ```bash
   git remote add origin https://gitlab.com/username/project_slug.git
   ```
4. Add files and push:
   ```bash
   git add .
   git commit -m "Initial commit"
   git push --set-upstream origin main
   ```

### Push an Existing Git Repository
1. Navigate to your repository:
   ```bash
   cd existing_repo
   ```
2. Configure the Git repository:
   ```bash
   git remote rename origin old-origin
   git remote add origin https://gitlab.com/username/project_slug.git
   ```
3. Push all branches:
   ```bash
   git push --set-upstream origin --all
   ```
4. Push all tags:
   ```bash
   git push --set-upstream origin --tags
   ```
