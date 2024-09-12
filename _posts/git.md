# Git and GitHub: Essential Tools for Computational Setup and Collaboration

## Introduction

In my experience collaborating with bioinformaticians, I've come to realize that Git and GitHub training and maintaining best practices are not always emphasized in core training programs, yet they are absolutely essential. Many companies prefer individuals who actively use Git and GitHub—not just as a portfolio, but as practical tools. It's not enough to have a series of repositories with projects uploaded at once without a clear Git history. This article will explore why Git is crucial for development and collaboration, and how understanding its features can make a significant difference in your workflow.

## What is Git?

Git is a distributed version control system used to track changes in source code during software development. It allows multiple people to work on a project simultaneously, merging their changes in a controlled manner. By maintaining a history of changes, Git ensures that developers can collaborate efficiently and revert to previous states if needed.

### Alternatives to Git

While Git is widely used, there are alternatives such as Mercurial and Subversion (SVN). However, Git's distributed nature and branching capabilities make it particularly well-suited for collaborative development.

## What is GitHub?

GitHub is a web-based platform that uses Git for version control. It provides a user-friendly interface for managing repositories, collaborating with others, and tracking issues. GitHub also offers features like pull requests, which facilitate code reviews and discussions about changes.

## GitLab vs. GitHub

Many companies use GitLab, which is another popular platform for Git repositories. GitLab offers similar features to GitHub but includes additional functionalities like integrated CI/CD pipelines. For this discussion, we'll focus on GitHub and general Git practices.

## Glossary

- **Repository**: A storage space for your project, including all its files and the entire version history.
- **Branch**: A parallel version of the repository. The main branch is typically called `main` or `master`.
- **Pull**: Fetches and integrates changes from a remote repository to your local repository.
- **Push**: Sends your committed changes to a remote repository.

## Basics

1. **Initialize a Repository**: `git init`
2. **Add Files**: `git add .`
3. **Commit Changes**: `git commit -m "Your message"`
4. **Push Changes**: `git push`

## Scenarios

### Scenario 1: Working on a Project Without Contributions

If you are working on a project independently:

1. **Clone the Repository**: `git clone <repository_url>`
2. **Fork the Repository**: Create a personal copy of the repository.
3. **Stay Up-to-Date**: Set up the upstream remote to keep your fork updated.
4. **Commit Changes**: Make changes and commit them to your fork.

### Scenario 2: Contributing and Collaborating

When collaborating with others:

1. **Create a Branch**: `git checkout -b branch_name`
2. **Commit Changes**: Commit changes to your branch. Best practices involve making updates that are coherent and focused, avoiding a series of unrelated updates.
3. **Rebase Main**: Update your branch with changes from the main branch. Be cautious as this changes the commit history. Only rebase if you are working on the branch alone. [Include diagram of tree before/after]
4. **Squash Commits**: Use squashing to combine multiple commits into one. This can be done using `git rebase -i`. [Include before and after commit messages, and how the tree looks]
5. **Merge**: Combine changes from your branch into the main branch while keeping all history. This is ideal for branches with frequent updates and multiple contributors.
6. **Push Changes**: `git push`
7. **Pull Request**: Create a pull request on GitHub to propose your changes. [Include screenshot]

## Handling Large Files

For large files such as language models:

1. **Download Git LFS (Large File Storage)**: `git lfs install`
2. **Track Large Files**: `git lfs track "*.file_extension"`
3. **Commit and Push**: Commit and push as usual.

## Best Practices

- **Branching Strategy**: Use branches for main (`main`), development (`dev`), features (`feature`), hotfixes (`hotfix`), and releases (`release`).
- **Feature Branches**: Squash commits before merging to keep the history clean.
- **Rebase with Caution**: Rebase only if you are sure it will not disrupt other collaborators.

By understanding these concepts and best practices, you'll be better equipped to manage your projects and collaborate effectively in a computational setup. Remember, Git and GitHub are not just tools—they are essential components of a successful development workflow.

