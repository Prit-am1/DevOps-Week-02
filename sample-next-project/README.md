# DevOps Week 02 — Git & GitHub Workflow

A hands-on DevOps project demonstrating practical **Git and GitHub collaboration workflows** using a sample **Next.js application**.

The project simulates a development environment where feature changes are developed independently, reviewed through Pull Requests, merged into the main branch, and conflicts are resolved before integration.

---

## 📌 Project Overview

The objective of this project is to practice source code management and collaborative development workflows commonly used by DevOps and software engineering teams.

A sample Next.js application is used as the project codebase while Git and GitHub are used for version control, branch management, collaboration, and code integration.

### Key objectives

* Manage application source code using Git
* Work with multiple feature branches
* Maintain isolated feature development
* Create meaningful Git commits
* Push local branches to GitHub
* Create and manage Pull Requests
* Merge feature branches into `main`
* Identify and resolve merge conflicts
* Synchronize local and remote repositories

---

## 🛠️ Technology Stack

| Technology   | Purpose                             |
| ------------ | ----------------------------------- |
| Next.js      | Sample web application              |
| React        | UI framework                        |
| TypeScript   | Application development             |
| Tailwind CSS | Styling                             |
| Git          | Distributed version control         |
| GitHub       | Remote repository and collaboration |
| Linux / WSL2 | Development environment             |
| npm          | Node.js package management          |

---

## 🌿 Branching Strategy

The project follows a simple feature-branch workflow.

```text
main
│
├── feature/update-homepage
│
└── feature/update-project-info
```

### `main`

Contains the stable and integrated version of the project.

### `feature/update-homepage`

Used to customize the default Next.js homepage with information about the DevOps project.

### `feature/update-project-info`

Used to introduce structured project information and additional application changes.

---

## 🔄 Git & GitHub Workflow

The development workflow followed throughout the project:

```text
Create Feature Branch
        ↓
Modify Application
        ↓
Review Changes
        ↓
Stage Changes
        ↓
Commit Changes
        ↓
Push Feature Branch
        ↓
Create Pull Request
        ↓
Review / Resolve Conflicts
        ↓
Merge into Main
        ↓
Synchronize Local Repository
```

This workflow keeps feature development isolated from the stable `main` branch until the changes are ready to be integrated.

---

## 🔀 Pull Request Workflow

Feature changes were pushed to GitHub and integrated through Pull Requests rather than directly merging every change into `main`.

The workflow included:

1. Creating a feature branch from `main`
2. Making application changes on the feature branch
3. Committing changes with meaningful commit messages
4. Pushing the branch to GitHub
5. Opening a Pull Request against `main`
6. Reviewing the differences between branches
7. Merging approved changes into `main`

---

## ⚠️ Merge Conflict Resolution

A merge conflict was intentionally created to practice real-world conflict resolution.

Both `main` and `feature/update-project-info` modified the same section of:

```text
sample-next-project/app/page.tsx
```

Git was unable to automatically determine which version should be retained and reported a content conflict.

The conflict was resolved manually by reviewing both versions and creating the final combined content.

The resolved file was then staged and committed to complete the merge:

```bash
git add sample-next-project/app/page.tsx
git commit
git push
```

This demonstrated the complete lifecycle of detecting, reviewing, resolving, and committing a merge conflict.

---

## 📂 Project Structure

```text
DevOps-Week-02/
│
└── sample-next-project/
    ├── app/
    │   ├── page.tsx
    │   ├── layout.tsx
    │   ├── globals.css
    │   └── project-info.ts
    │
    ├── public/
    ├── package.json
    ├── package-lock.json
    ├── next.config.ts
    ├── tsconfig.json
    └── README.md
```

---

## 🚀 Running the Application

### 1. Clone the repository

```bash
git clone <repository-url>
```

### 2. Navigate to the Next.js application

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

The application will normally be available at:

```text
http://localhost:3000
```

---

## 📚 Git Concepts Practiced

This project provides hands-on practice with:

* Repository initialization
* Working directory and staging area
* Git commits
* Local and remote repositories
* Feature branches
* Remote-tracking branches
* `git fetch`
* `git pull`
* `git push`
* Branch merging
* Pull Requests
* Divergent branches
* Merge conflicts
* Manual conflict resolution
* Local and remote synchronization

---

## 🎯 Learning Outcome

Through this project, a complete feature-based Git and GitHub workflow was implemented using a real application codebase.

The exercise demonstrates how developers and DevOps engineers can work on isolated changes, collaborate through GitHub, integrate features safely, handle conflicting changes, and maintain a synchronized `main` branch.

---

## 👤 Author

**Pritam Roy Chowdhury**

DevOps & Cloud Engineering Practice Project

