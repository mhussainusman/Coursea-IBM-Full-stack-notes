# Course 4: Getting Started with Git and GitHub
## Module 1: Git and GitHub Fundamentals

### Key Concepts
- **Branch**: A snapshot of your repository to which you can make changes.
- **Child Branch**: A branch where you can build, edit, and test changes before merging.
- **Main Branch**: The primary branch where final changes are merged.
- **Multiple Branches**: Used to allow multiple team members to work without conflicts.
- **Pull Request**: A notification to team members about changes made for review and merging.

### Notes
In this module, you learned about the fundamental concept of branches in Git and GitHub. A branch represents a snapshot of your repository that allows you to make changes independently from the main branch. This enables developers to work on features, fixes, or experiments in isolation.

The child branch is where you can build, edit, and test your changes safely. Once the changes are ready and verified, they can be merged back into the main branch, which is the central version of the project. Using multiple branches helps prevent conflicts and ensures that one member's work does not impede or affect the workflow of others.

To collaborate effectively, pull requests are used to notify team members about proposed changes, allowing for review and discussion before merging.

### Code Examples
```bash
# Create a new branch named "feature-branch"
git branch feature-branch

# Switch to the new branch
git checkout feature-branch

# Make changes, then add and commit them
git add .
git commit -m "Add new feature"

# Switch back to main branch
git checkout main

# Merge the feature branch into main
git merge feature-branch

# Push changes to remote repository
git push origin main
```

### Cheat Sheet
| Concept | Syntax / Example | Description |
|---|---|---|
| Branch | `git branch [branch-name]` | Create a new branch |
| Switch Branch | `git checkout [branch-name]` | Move to a different branch |
| Commit | `git commit -m "message"` | Save changes with a message |
| Merge | `git merge [branch-name]` | Combine changes from one branch into another |
| Pull Request | GitHub UI feature | Request to merge changes after review |

### Glossary
- **Branch**: A separate line of development in a repository.
- **Child Branch**: A branch created from the main branch for isolated work.
- **Main Branch**: The primary branch where the stable code resides.
- **Pull Request**: A request to merge changes from one branch into another, typically reviewed by team members.

### Summary
This module introduced the concept of branches in Git and GitHub, explaining how they enable isolated development and collaboration. It covered how to create, switch, and merge branches, and the role of pull requests in team workflows. Understanding these fundamentals is essential for effective version control and collaborative software development.