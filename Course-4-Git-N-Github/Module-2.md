# Course 4: Getting Started with Git and GitHub
## Module 2: Git Commands and Managing GitHub Projects

### Key Concepts
- **Git clone**: Copy a remote repository to local machine.
- **Git fork**: Create an independent copy of a repository for new projects.
- **Git branch**: Create separate lines of development.
- **Git add**: Stage changes for commit.
- **Git commit**: Save changes to local repository.
- **Git push**: Upload local commits to remote repository.
- **Git pull**: Update local repository with remote changes.
- **Git fetch**: Retrieve remote changes without merging.
- **Git merge**: Combine changes from different branches.
- **Git revert**: Undo changes by creating a new commit.
- **Roles in Git projects**: Developer, Integrator, Repository Administrator.

### Notes
This module covers essential Git commands and workflows for managing projects on GitHub. You learn how to clone repositories to work locally and fork repositories to create independent projects. Branching allows parallel development, and changes are staged with `git add` before committing locally with `git commit`.

To share changes, you push commits to the remote repository. Keeping your local repository updated involves pulling or fetching changes from the remote. Merging integrates changes from different branches, while reverting undoes changes by creating new commits.

The module also explains the roles involved in project management: Developers write code and use commands like clone, pull, and push; Integrators review and merge changes; Repository Administrators manage repository settings and access. Understanding these commands and roles is crucial for effective collaboration and version control in software projects.

### Code Examples
```bash
# Clone a remote repository
git clone https://github.com/user/repo.git

# Create and switch to a new branch
git checkout -b feature-branch

# Stage all changes
git add .

# Commit staged changes with a message
git commit -m "Add new feature"

# Push commits to remote branch
git push origin feature-branch

# Pull latest changes from remote
git pull origin main

# Fetch changes without merging
git fetch origin

# Merge a branch into current branch
git merge feature-branch

# Revert a commit by its hash
git revert abc1234
```

### Cheat Sheet
| Concept | Syntax / Example | Description |
|---|---|---|
| Clone | `git clone <repo-url>` | Copy remote repository locally |
| Fork | Use GitHub UI to fork | Create independent copy of a repository |
| Branch | `git checkout -b <branch-name>` | Create and switch to a new branch |
| Add | `git add <file>` or `git add .` | Stage changes for commit |
| Commit | `git commit -m "message"` | Save staged changes locally |
| Push | `git push origin <branch>` | Upload commits to remote repository |
| Pull | `git pull origin <branch>` | Update local repo with remote changes |
| Fetch | `git fetch origin` | Retrieve remote changes without merging |
| Merge | `git merge <branch>` | Combine changes from another branch |
| Revert | `git revert <commit-hash>` | Undo changes by creating a new commit |

### Glossary
- **Clone**: Copying a remote repository to your local machine.
- **Fork**: Creating an independent copy of a repository to work on separately.
- **Branch**: A separate line of development within a repository.
- **Commit**: A saved snapshot of changes in the local repository.
- **Push**: Uploading local commits to a remote repository.
- **Pull**: Fetching and merging changes from a remote repository to local.
- **Fetch**: Downloading changes from remote without merging.
- **Merge**: Combining changes from different branches.
- **Revert**: Creating a new commit that undoes changes from a previous commit.
- **Developer**: Role responsible for writing code and pushing changes.
- **Integrator**: Role responsible for reviewing and merging changes.
- **Repository Administrator**: Role managing repository settings and access.

### Summary
This module introduces key Git commands and workflows essential for managing and collaborating on GitHub projects. It explains how to clone, fork, branch, commit, push, pull, fetch, merge, and revert changes, as well as the roles involved in project management. Mastery of these concepts enables effective version control and teamwork in software development.