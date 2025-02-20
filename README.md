# Git Project Setup Documentation
## Table of Contents
- [Git Setup](#local-git-setup)
  - [Configure Git Identity for the Current Project](#configure-git-identity-for-the-current-project)
- [Global Git Setup](#global-git-setup)
  - [Configure Git Identity Globally for All Projects](#configure-git-identity-globally-for-all-projects)
- [Git Origin Remove](#git-origin-remove)
- [Add Files and Push to Repository](#add-files-and-push-to-repository)
  - [HTTPS](#https)
    - [Create a New Repository](#create-a-new-repository)
    - [Push an Existing Folder to the Repository](#push-an-existing-folder-to-the-repository)
    - [Push an Existing Git Repository](#push-an-existing-git-repository)

## Local Git Setup
### Configure Git Identity for the Current Project
```bash
git config --local user.name "username"
git config --local user.email "user@gmail.com"
```

## Global Git Setup
### Configure Git Identity Globally for All Projects
```bash
git config --global user.name "username"
git config --global user.email "user@gmail.com"
```

## Git Origin Remove (don't do it)
```bash
git remote rm origin
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
