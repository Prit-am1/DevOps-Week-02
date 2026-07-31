# 🚀 DevOps Week 02 — Git & GitHub Workflow

![Git](https://img.shields.io/badge/Git-Version%20Control-F05032?logo=git\&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Collaboration-181717?logo=github)
![Next.js](https://img.shields.io/badge/Next.js-Sample%20Application-000000?logo=nextdotjs)
![TypeScript](https://img.shields.io/badge/TypeScript-Application-3178C6?logo=typescript\&logoColor=white)

A hands-on **DevOps source-code management project** demonstrating practical Git and GitHub workflows using a sample Next.js application.

The repository simulates a collaborative development environment where application changes are developed on isolated feature branches, committed and pushed to GitHub, reviewed through Pull Requests, merged into the main branch, and synchronized between local and remote repositories.

The project also demonstrates the complete process of identifying and manually resolving a **Git merge conflict**.

---

## 📌 Project Overview

The objective of this project is to gain practical experience with the Git and GitHub workflows commonly used by development and DevOps teams.

Rather than practicing Git commands on isolated text files, a real **Next.js application** is used as the source-code repository.

### Key Objectives

* Manage application source code using Git
* Work with local and remote repositories
* Create and manage feature branches
* Keep feature development isolated from `main`
* Write meaningful Git commits
* Push branches to GitHub
* Create and manage Pull Requests
* Merge completed features into `main`
* Synchronize local and remote branches
* Understand divergent Git histories
* Identify and manually resolve merge conflicts
* Maintain clear project documentation

---

## 🛠️ Technology Stack

| Technology                | Purpose                                             |
| ------------------------- | --------------------------------------------------- |
| **Git**                   | Distributed version control                         |
| **GitHub**                | Remote repository, Pull Requests, and collaboration |
| **Next.js**               | Sample application used as the project codebase     |
| **React**                 | Frontend UI library                                 |
| **TypeScript**            | Application development                             |
| **Tailwind CSS**          | Application styling                                 |
| **Node.js / npm**         | JavaScript runtime and package management           |
| **Linux (Ubuntu / WSL2)** | Local development and Git environment               |

---

## 📂 Repository Structure

```text
DevOps-Week-02/
│
├── README.md
│
└── sample-next-project/
    │
    ├── app/
    │   ├── globals.css
    │   ├── layout.tsx
    │   ├── page.tsx
    │   └── project-info.ts
    │
    ├── public/
    ├── package.json
    ├── package-lock.json
    ├── next.config.ts
    ├── tsconfig.json
    └── ...
```

The Git repository is maintained at the `DevOps-Week-02` level, while the Next.js application is contained inside `sample-next-project`.

---

## 🌿 Branching Strategy

A simple **feature-branch workflow** was used throughout the project.

```text
main
│
├── feature/update-homepage
│
└── feature/update-project-info
```

### `main`

The primary branch containing the stable and integrated version of the application.

### `feature/update-homepage`

Created to replace the default Next.js homepage with project-specific content.

### `feature/update-project-info`

Created to add structured project information and additional application changes.

After feature development was completed, the branches were pushed to GitHub and integrated into `main` through Pull Requests.

---

## 🔄 Development Workflow

The project followed this Git and GitHub workflow:

```text
              main
                │
                ▼
       Create Feature Branch
                │
                ▼
         Modify Application
                │
                ▼
          Review Changes
           (git diff)
                │
                ▼
           Stage Changes
            (git add)
                │
                ▼
          Commit Changes
          (git commit)
                │
                ▼
        Push Feature Branch
            (git push)
                │
                ▼
       Create Pull Request
                │
                ▼
       Review / Resolve Issues
                │
                ▼
          Merge into main
                │
                ▼
       Synchronize Repository
```

This workflow ensures that feature development remains isolated until the changes are ready to be integrated into the stable branch.

---

## 🔀 Pull Request Workflow

Application changes were integrated through **GitHub Pull Requests**.

The general workflow was:

1. Start from an updated `main` branch.
2. Create a dedicated feature branch.
3. Modify the application.
4. Review changes using `git status` and `git diff`.
5. Stage the required files.
6. Create a meaningful commit.
7. Push the feature branch to GitHub.
8. Open a Pull Request against `main`.
9. Review the branch differences.
10. Resolve conflicts when necessary.
11. Merge the Pull Request.
12. Synchronize the local `main` branch with GitHub.

This prevents unfinished feature work from being directly introduced into the stable branch.

---

## ⚠️ Merge Conflict Resolution

A merge conflict was intentionally created to understand how Git handles competing changes.

Both `main` and `feature/update-project-info` modified the same section of:

```text
sample-next-project/app/page.tsx
```

The feature branch contained:

```text
Git and GitHub Collaboration Practice
```

while `main` contained:

```text
Git and GitHub Workflow Hands-on Project
```

Because both branches modified the same original line differently, Git could not automatically determine which change should be retained.

Git reported the conflict using conflict markers similar to:

```text
<<<<<<< HEAD
Git and GitHub Collaboration Practice
=======
Git and GitHub Workflow Hands-on Project
>>>>>>> main
```

The conflict was manually reviewed and resolved by combining the intended changes into:

```text
Git and GitHub Collaboration & Workflow Practice
```

The resolved file was then staged:

```bash
git add sample-next-project/app/page.tsx
```

and the merge was completed with a merge commit.

The resolved feature branch was pushed back to GitHub, allowing the Pull Request to be successfully merged into `main`.

---

## 🧠 Git Concepts Practiced

The project provided hands-on experience with:

* Repository initialization
* Working directory
* Staging area
* Local repository
* Remote repository
* Local branches
* Remote branches
* Remote-tracking branches
* Feature-branch workflow
* Git commits
* Branch switching
* Fetching remote changes
* Pulling remote changes
* Pushing local changes
* Pull Requests
* Branch merging
* Fast-forward concepts
* Divergent branches
* Merge strategies
* Merge conflicts
* Conflict markers
* Manual conflict resolution
* Merge commits
* Local and remote synchronization

### Git Commands Used

```bash
git init
git status
git diff
git add
git commit
git branch
git switch
git fetch
git pull
git push
git remote
git log
```

---

## 🚀 Running the Application

### 1. Clone the repository

```bash
git clone <repository-url>
```

### 2. Enter the Next.js project

```bash
cd DevOps-Week-02/sample-next-project
```

### 3. Install dependencies

```bash
npm install
```

### 4. Start the development server

```bash
npm run dev
```

The development server will normally be available at:

```text
http://localhost:3000
```

---

## 📈 Project Workflow Summary

```text
Repository Initialization
        │
        ▼
Initial Next.js Commit
        │
        ▼
Feature Branch #1
        │
        ▼
Homepage Modification
        │
        ▼
Pull Request #1
        │
        ▼
Merge into main
        │
        ▼
Feature Branch #2
        │
        ▼
Project Information Added
        │
        ▼
Pull Request #2
        │
        ▼
Intentional Merge Conflict
        │
        ▼
Manual Conflict Resolution
        │
        ▼
Merge into main
        │
        ▼
README Documentation
        │
        ▼
Final Repository Synchronization
```

---

## 🎯 Learning Outcome

This project demonstrates an end-to-end Git and GitHub collaboration workflow using a real application codebase.

By completing the project, practical experience was gained in managing feature development, maintaining branch isolation, synchronizing local and remote repositories, creating Pull Requests, integrating application changes, and resolving conflicting code changes.

The project provides a foundation for more advanced DevOps workflows involving **CI/CD pipelines, containerization, Infrastructure as Code, and automated deployment processes**.

---

## 👤 Author

**Pritam Roy Chowdhury**

DevOps & Cloud Engineering Practice Project
