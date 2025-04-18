# Git-and-Github-for-absolute-beginners 
Here i am sharing all my learning about git and git hub which is for beginners.

---

## 🌟 Learning Roadmap
For a complete beginner's path, check out:  
[Git/GitHub Roadmap for Beginners](https://roadmap.sh/git-github?r=git-github-beginner)
## OR you can continue from here it covers all the things mentioned on the roadmap.
---
## LEARNING BASICS 

## 1. What are Version Control Systems (VCS)?

A VCS is a tool that tracks changes to your files (like code or documents) over time. It lets you:

### Key Benefits:
- **Save versions** of your work (like "save points" in a game)
- **Revert** to older versions if you make a mistake
- **Collaborate** with others on the same project without conflicts

### Popular Example:
Git (the tool behind GitHub) is the most widely used VCS.

## 2. What is Git and why should you use it?

Git is a free, open-source version control system (VCS) that helps you:

### Key Features:
- **Track changes** in your code/files over time (like a "time machine")
- **Collaborate** with others without overwriting each other's work
- **Recover** old versions if something breaks

### Why Use Git?
✅ **Undo Mistakes** - Accidentally deleted code? Git lets you restore it  
✅ **Teamwork** - Multiple people can work simultaneously (using branches)  
✅ **Organization** - Keeps history of who changed what and why  
✅ **GitHub/GitLab** - Share code and contribute to open-source projects  
✅ **Jobs Requirement** - Used by nearly all professional developers

## 3. How to Install Git Locally

### Windows
1. Download Git from [git-scm.com](https://git-scm.com/download/win)
2. Run the installer (.exe file)
3. Follow setup steps (keep default options)
4. Verify installation in Command Prompt:
   ```cmd
   git --version

### MAC OS
 https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh

## 4. Create a GITHUB account?
Assuming you have created it or you can follow the below steps:
## Step-by-Step Guide

1. Go to [GitHub's signup page](https://github.com/signup)

2. Enter your details:
   • Email address (use one you can access)  
   • Password (create a strong one)  
   • Username (this will be your GitHub handle)  

3. Verify your account:
   • GitHub will send a verification code to your email  
   • Enter the code on the verification page  

4. Complete setup:
   • Choose your plan (Free plan is sufficient for beginners)  
   • Answer optional survey questions (or skip)  

5. Start using GitHub!  

---

## First Steps After Signup
• Set up your profile picture in **Settings**  
• Create your first repository:  
  ```
  [New] > [Repository] > Name it (e.g., "my-first-project")
  ```

---

# Git & GitHub Basics

## Essential Git Commands

### 1. Initialize a Repository
```bash
git init
```
Creates a new Git repository in your current folder.

### 2. Stage Changes
```bash
git add .
```
Stages all changed files. Use `git add filename` for specific files.

### 3. Commit Changes
```bash
git commit -m "Your commit message"
```
Saves your staged changes with a description.

### 4. Undo Changes
```bash
git reset HEAD filename
```
Unstages a file while keeping your changes.

### Branching
```bash
git branch new-feature     # Create branch
git checkout new-feature  # Switch branch
git merge new-feature     # Merge changes
```

---

## GitHub Integration
### Repository Setup
1. Create new repo on GitHub (public/private)
2. Connect local repo:
```bash
git remote add origin https://github.com/your/repo.git
git push -u origin main
```
3. Add links:
```bash
Go to [GitHub's signup page](https://github.com/signup)
```
  You can add normal link directly , and aslo use can use this type of line in README.md, the part under square brackets[] is your links specific name and under normal brackets() the normal link now this link will not show in the preview section.
  
### Repository Page
![image](https://github.com/user-attachments/assets/c72de739-5645-4fae-8788-dab27d29549e)

### Daily Workflow
```bash
git pull                 # Get latest changes
git add .
git commit -m "Changes"
git push
```

## Pro Tips
- Use `git status` frequently
- Write clear commit messages
- Pull before you push to avoid conflicts

---

## let's learn how git handels our files/folders
```
When you create a folder on your computer, Git doesn’t automatically track it.
To start using Git with that folder, you first need to initialize it (run git init).
This gives Git permission to manage the folder, allowing it to track files, detect modifications, stage changes, and save checkpoints (commits).
```
![image](https://github.com/user-attachments/assets/a80755fa-50db-45d5-81af-b32e93624e9d)

- To check which files are on which stage ➡️ ``` git status -s ```
- To check how many save points are there ➡️ ``` git log--oneline ``` or ``` git log- ```
---
- Step 1 - intilise the folder.
  
  ![image](https://github.com/user-attachments/assets/dd0ddffb-b8a9-4c2c-af59-0a6b2e6cec2b)
  
  click on the third icon(Source control icon) in vs code  and click intialize, this image in above is after intialization.
- Step 2 - Now you can check the folder is initialise or not in terminal by writting ``` git status -s ```
  ![image](https://github.com/user-attachments/assets/ea717b73-0ea7-407c-a827-0771f2577e8f)
  ![image](https://github.com/user-attachments/assets/99c573d4-d3d3-4896-8bc0-6b36e16d41b7)

