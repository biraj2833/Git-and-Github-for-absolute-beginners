# Git-and-Github-for-absolute-beginners 
Here i am sharing all my learning about git and git hub which is for beginners. If you saw any mistakes kindly give a pull request.

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
- ![image](https://github.com/user-attachments/assets/ee8b45fc-6638-4818-9348-9857a6c0773b)
   - if it is not initialised this "??" symbol will show ⬆️
     
   - and if it is initialised this type of symbol will show up. ⬇️
 
  ![image](https://github.com/user-attachments/assets/ea717b73-0ea7-407c-a827-0771f2577e8f)
  ![image](https://github.com/user-attachments/assets/99c573d4-d3d3-4896-8bc0-6b36e16d41b7)

---

# 🌿 Git Branching Guide

## What is a Branch?
A **branch** is a parallel version of your repository. It lets you:
- Work on new features without breaking the main code (`main`/`master` branch)
- Experiment safely
- Collaborate without conflicts

## Key Commands

### 1. Create & Switch to a New Branch
```bash
git switch -b feature/new-login  # Creates and switches to new branch
```

## Git Branch Creation: `git switch -b` vs `git branch`

### 🔄 Key Difference
| Command | Creates Branch? | Switches to Branch? | Recommended Use |
|---------|----------------|---------------------|-----------------|
| `git switch -b feature/new-feature` | ✅ Yes | ✅ Yes | When you want to **create AND start working** immediately |
| `git branch feature/new-feature` | ✅ Yes | ❌ No | When you want to create but **stay on current branch** |

---

## 🛠️ Detailed Comparison

#### 1. `git switch -b feature/new-feature`
```bash
git branch feature/login-page  # Only creates
git switch feature/login-page  # Need this to actually use it
```
# Git Switch Flags: `-b`, `-c`, `-d` Explained

## 🌿 Basic Flags Comparison
| Flag | Command Example | Purpose | Notes |
|------|-----------------|---------|-------|
| `-b` | `git switch -b new-feature` | **Create and switch** to new branch | Legacy (works in all Git versions) |
| `-c` | `git switch -c new-feature` | **Create and switch** to new branch | Newer alias for `-b` (Git 2.23+) |
| `-d` | `git switch -d old-feature` | **Delete** a branch after switching away | Safety check: won't delete unmerged changes |

---

## Detailed Breakdown

### 1. `-b` (Base)
```bash
git switch -b feature/login
```

![image](https://github.com/user-attachments/assets/5f9df443-ed3e-496c-8478-06ea354c5f9e)
![image](https://github.com/user-attachments/assets/16aedf8b-f284-4e8d-bff4-0278998b825c)

---

# 🔀 Git Merging Guide

## Types of Merges

### 1. Fast-Forward Merge
```bash
git checkout main
git merge feature/login
```
- When: Branch has no divergent commits
- Result: Linear history (no merge commit)

# Three way merging
```bash
git checkout main
git merge --no-ff feature/login  # Forces merge commit
```
- When: Branches have diverged
- Result: Creates new merge commit

Here's a concise comparison table of Fast-Forward (FF) vs Three-Way merges in GitHub-flavored Markdown for your `README.md`:

# 🔀 Git Merge Strategies Comparison

| Feature               | Fast-Forward Merge                | Three-Way Merge                  |
|-----------------------|-----------------------------------|----------------------------------|
| **Trigger Condition** | Target branch has no new commits  | Branches have diverged           |
| **Command**           | `git merge feature-branch`        | `git merge --no-ff feature-branch` |
| **History**           | Linear (no merge commit)          | Non-linear (creates merge commit) |
| **Visualization**     | Straight line                     | Merge "bubble" in git log        |
| **Conflict Risk**     | None                              | High (requires resolution)       |
| **Best For**          | • Short-lived branches<br>• Solo work<br>• Bug fixes | • Team collaborations<br>• Long-running features<br>• Audit trails |
| **GitHub UI Default** | "Rebase and merge" option         | "Create merge commit" option     |
| **Performance**       | Faster (pointer move only)        | Slower (needs diff calculation)  |
| **Traceability**      | Harder to identify merges         | Clear merge points in history    |


## When to Use Which?

### Fast-Forward (FF)
```bash
git config --global merge.ff only  # Enforce FF when possible
```
✅ Small fixes  
✅ Release branches  
✅ CI/CD pipelines requiring linear history  

### Three-Way
```bash
git merge --no-ff feature/auth
```
✅ Feature toggles  
✅ Team development  
✅ Important version integrations  

 📚 **Pro Tip**: Use `git log --graph --oneline` to visualize merge strategies!

### Key Notes:
1. **Force FF**: `--ff-only` aborts if not possible
2. **Force 3-way**: `--no-ff` always creates merge commit
3. **GitHub**: PR merge buttons map to these strategies

# Stashing

![image](https://github.com/user-attachments/assets/ba1a0a3c-69ae-4c52-b82c-c781ea41b0f3)
![image](https://github.com/user-attachments/assets/aacd4a7c-c2e2-4eb3-bbdc-c8026fc4299e) 
If you edit a file and dont commit the changes, now if you change the branch [( ``` git switch feature/stashing ``` ) feature/stashing is the file name ]without commiting your file git tell you to commit the changes or stash them ,  
we can use ``` git stash ``` to save the changes or stash the file. 
now if you again switch into the main branch (``` git switch main```) you can't see the changes until you applt them by (``` git stash apply```).
And now if you want to delete the stash memory (``` git stash clear```).

# Collaboration 
We can collaborates with other on a project using git hub.
   1. The main guy will intialize the repository and make folder in it and then upload it on github.
   2. And he also have add colaboraters in the repo from ``` settings -> add collaborator ```.
   3. Another team members can now download it.
   4. firtly all guys have to make their own branches and then do their work on thier own branch it is very important steps either wise the project will get messed up.
   5. Then every one can commit their work and give a pull request.
   6. Now the main guy can see the pull request and if want he can merge it to the main project.
   7. ![image](https://github.com/user-attachments/assets/860b4bbf-9a44-4fb6-bffc-81d8af63fe46)
      
