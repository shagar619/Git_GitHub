# Git & Github


## 🧰 What is Git?

**Git** is a **version control system**. It helps developers track and manage changes to code over time.

- Developed by **Linus Torvalds** (the creator of Linux) in **2005**.
- Works locally on your computer.
- Keeps a history of all changes to files.
- Lets you create branches to work on different features or bug fixes without affecting the main codebase.
- Helps teams collaborate by merging changes from multiple people.

🔧 Think of Git as a **tool** you use on your computer to keep track of project changes.

---

## 🌐 What is GitHub?

**GitHub** is a **cloud-based hosting service** for Git repositories.

- Owned by **Microsoft**.
- Provides a web interface to store, share, and collaborate on Git projects.
- Adds features like:
  - Pull requests (to propose code changes)
  - Issue tracking (for bugs or tasks)
  - Project management tools
  - Access control (who can view or edit code)
- Makes it easy for teams (or open-source communities) to work together online.

🌍 Think of GitHub as a **social platform + cloud storage** for Git repositories.

---

## 🔍 Key Differences

| Feature              | Git                                  | GitHub                                      |
|----------------------|---------------------------------------|----------------------------------------------|
| Type                 | Tool (command-line based)             | Hosting platform (web-based)                |
| Usage                | Local version control                 | Remote code sharing and collaboration       |
| Requires Internet?   | No (except for pushing/pulling)       | Yes                                          |
| Main Purpose         | Track code changes locally            | Host Git repositories and collaborate online|
| Creator              | Linus Torvalds                        | GitHub, Inc. (now owned by Microsoft)       |

---

## ✅ Summary

- **Git** is the engine that powers version control.
- **GitHub** is like a garage where you store and show off your code engine to others.


## Git Commands


## 🔹 `git init` — Initialize a Git Repository

### 📖 Definition

The command : `git init`


is used to **create a new Git repository** in your project directory. It sets up everything Git needs to start tracking changes to your code.

---

### ⚙️ What Happens When You Run `git init`?

- Git creates a hidden directory called **`.git/`** inside your project folder.
- This `.git` folder contains all the internal metadata and history that Git uses to manage the repository.
- Your folder is now a **local Git repository**, meaning Git can start tracking file changes, commits, branches, etc.

---

### 🧪 Example

- `mkdir my-project`
- `cd my-project`
- `git init`

After running these commands:

- You’ll see nothing new in the folder (since `.git` is hidden).
- But behind the scenes, Git is now watching your project.

---

### 🧠 Why Use It?

- To start version controlling a new or existing project.
- To work with Git commands like `git add`, `git commit`, `git status`, etc.

---


### ⚠️ Note

- `git init` **does not connect to GitHub** or any remote repository.
- To link it to a GitHub repo later, you'd use:

---
---
---


## 🔹 `git add` — Add Changes to the Staging Area

### 📖 Definition

The command : `git add <file-or-directory>`


is used to **add changes from your working directory to Git’s staging area**. This means you are telling Git which changes you want to include in the next commit.

---

### ⚙️ What Happens When You Run `git add`?

- Git tracks the specified files or directories and marks their current state to be included in the next commit.
- Changes are **not yet saved permanently**; they’re just prepared for committing.
- You can add individual files or all changes at once (using `git add .` or `git add -A`).

---

### 🧪 Examples

Add a single file : `git add README.md`


Add all changed files in the current directory and subdirectories : `git add .`



---

### 🧠 Why Use It?

- To control exactly which changes you want to save in your project history.
- It lets you review or group changes logically before committing.
- Allows partial commits by adding only some files or parts of files.

---

### ⚠️ Note

- Files must be staged with `git add` before you can commit them with `git commit`.
- If you forget to add changes, they won’t be saved in your commit.

---
---
---

## 🧰 `git commit` — Save Changes to the Repository

### 📖 Definition

The command : `git commit -m "commit message"`



is used to **save the staged changes permanently in the Git repository’s history** with a descriptive message.

---

### ⚙️ What Happens When You Run `git commit`?

- Git takes all the changes you’ve added to the staging area (using `git add`) and bundles them into a **commit**.
- A commit is like a **snapshot** of your project at that moment.
- Each commit has:
  - A unique ID (hash)
  - Author information
  - Timestamp
  - Your commit message describing the changes
- Commits let you track progress, revert to earlier versions, or collaborate with others.

---

### 🧪 Example

`git commit -m "Add README file with project description"`

---

### 🧠 Why Use It?

- To save your work in discrete, meaningful steps.
- To keep a history of what changes were made and why.
- To enable collaboration by sharing commits with others.

---

### ⚠️ Note

- You **must stage** files first using `git add` before committing.
- You can use just `git commit` (without `-m`) to open a text editor to write a longer commit message.


---
---
---


## 🔹 `git branch` — Work with Branches in Git

### 📖 Definition

The command : `git branch`


is used to **create, list, or delete branches** in a Git repository. A **branch** is a separate line of development that allows you to work on features, bug fixes, or experiments without affecting the main code.

---

### ⚙️ What Can `git branch` Do?

| Command                          | Description                                  |
|----------------------------------|----------------------------------------------|
| `git branch`                     | List all branches in the current repository  |
| `git branch <branch-name>`      | Create a new branch                          |
| `git branch -d <branch-name>`   | Delete a branch                              |
| `git branch -m <new-name>`      | Rename the current branch                    |
| `git branch -a`                 | List all branches, including remote ones     
|  `git checkout <branch-name>` | To switch a branch |
| `git checkout -b <branch-name>` | To create and switch to a new branch |
| `git checkout <branch-name>` | To switch to an existing branch |
| `git checkout --track origin/branch-name` | To create a branch and switch to it |
| `git checkout -` | To switch to the branch you were on before |
| `git checkout -b <branch-name> <commit-hash>` | To switch to a branch and reset it to a specific commit |
| `git checkout -b <branch-name> <branch-name>` | To switch to a branch and merge it with the current branch |
| `git branch --merged` | Show branches already merged into the current branch |
| `git branch --no-merged` | Show branches not yet merged into the current branch |
| `git branch --set-upstream-to=<remote>/<branch> <local-branch>` | Set the upstream (tracking) branch |
| `git branch -u <remote>/<branch> <local-branch>` | Short form of the above |
| `git show-branch` | Show commits from multiple branches in a summarized format |
| `git branch -vv` | Show commits from multiple branches in a summarized format |
| `git branch --contains <commit>` | List branches that contain a specific commit |
| `git branch --sort=<key>` | Sort branches (e.g., by `committerdate`, `authordate`) |
| `git branch --format="..."` | Customize the output (e.g., show only branch names or formats) |

---

### 🧪 Examples

- List all branches : `git branch`

- Create a new branch : `git branch feature-login`

- Delete a branch : `git branch -d feature-login`

- Rename the current branch : `git branch -m main`

- List all branches, including remote ones : `git branch -a`
---

### 🧠 Why Use It?

- To work on new features or fixes without touching the main project.
- To isolate code changes until you're ready to merge them.
- To experiment safely without breaking the main codebase.

---

### ⚠️ Note

- Creating a branch doesn’t automatically switch you to it.
- To switch branches, use:

---
---
---

## 🔹 `git remote` — Manage Connections to Remote Repositories

### 📖 Definition

The command : `git remote`

is used to **view and manage remote repositories**. A **remote repository** is a version of your project hosted on the internet or another network (like GitHub, GitLab, etc.).

Git uses remotes so you can **push** your changes to and **pull** updates from a shared repository.

---

### ⚙️ What Can `git remote` Do?

| Command                                      | Description                                           |
|---------------------------------------------|-------------------------------------------------------|
| `git remote`                                 | Lists short names of all configured remotes           |
| `git remote -v`                              | Lists remote names with their full URLs               |
| `git remote add <name> <url>`                | Adds a new remote connection                         |
| `git remote remove <name>`                   | Removes a remote                                     |
| `git remote rename <old> <new>`              | Renames a remote                                     |
| `git remote show <name>`                     | Shows detailed info about a specific remote          |
| `git remote set-url <name> <url>`            | Changes the URL for a remote                           |
| `git remote set-url --push <name> <new-url>` | Changes the push URL specifically (if different from fetch URL) |
| `git remote set-url --add <name> <url>`      | Adds a new URL to a remote                            |
| `git remote set-url --delete <name> <url>`   | Deletes a URL from a remote                           |
| `git remote update`                          | Fetches and merges the latest changes from remotes     |
| `git remote get-url <name>` | Shows the fetch URL of the remote|
| `git remote get-url --push <name>` | Shows the push URL of the remote|
| `git remote show <name>` | Displays detailed information about the specified remote, such as branches tracked and fetch/push configurations|
| `git remote prune <name>` | Removes stale references to remote branches that no longer exist |


---

### 🧪 Examples

Add a new remote (e.g., GitHub) : `git remote add origin https://github.com/username/project.git`

View all remotes and their URLs : `git remote -v`

Remove a remote : `git remote remove origin`

Rename a remote : `git remote rename origin upstream`

---

### 🧠 Why Use It?

- To connect your local repository to a remote one on platforms like GitHub, GitLab, or Bitbucket.
- To collaborate with others by pushing and pulling code.
- To manage multiple remotes (e.g., `origin`, `upstream`, etc.).

---

### ⚠️ Note

- The default remote is usually named `origin`.
- After adding a remote, you can push your code using: