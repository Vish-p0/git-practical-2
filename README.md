# Version Controlling with Git - II

## Introduction

This practical covers one of the most important and useful features in Git: **branching**. Along with branching, we will also learn about a simple workflow (branching strategy) and a concept called **Pull Requests (PRs)**.

---

## Step 1 – Individual Work

### 1. Create a Public GitHub Repository
- Go to [GitHub](https://github.com) and create a new public repository

### 2. Clone the Repository
```bash
git clone <https://repo_url>
```

### 3. Create a Feature Branch
There are two options for creating a branch:

**Option A:** Create branch and checkout separately
```bash
git branch <meaningful_branch_name>
git checkout <new_branch>
```

**Option B:** Create and switch in one command
```bash
git checkout -b <meaningful_branch_name>
```

> **Naming Convention:** Use a meaningful branch name following a good naming convention.
> Example: `git checkout -b feature/vishan.j/awesome-feature-x-to-our-app`

### 4. Add Files to the Branch
- Add some text files or HTML files to this branch (content doesn't matter)

### 5. Commit Changes Locally
```bash
git add .
git commit -m "Your commit message"
```

### 6. Push Branch to Remote
```bash
git push origin <branch_name>
```
- Verify your changes are available in the remote repository on GitHub under your feature branch name

### 7. Create a Pull Request
- Use the [GitHub official documentation](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) to create a Pull Request on GitHub for your branch

### 8. Merge the Pull Request
- Merge the pull request to the main branch by referring to [this official documentation](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/merging-a-pull-request)

---

## Step 2 – Collaborating with Another Colleague (Pair Work)

### 1. Add a Collaborator
- Pair up with a colleague and add them to your repository as a collaborator
- Refer to [this documentation](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository)

### 2. Clone Their Repository
```bash
git clone <colleague_repo_url>
```

### 3. Create a Branch and Make Changes
```bash
git checkout -b feature/<your_name>/<feature_description>
```
- Introduce a small change

### 4. Push the Branch to Remote
```bash
git push origin <branch_name>
```

### 5. Create a Pull Request
- Use the [GitHub official documentation](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) to create a Pull Request

### 6. Merge the Pull Request
- Merge the pull request to the main branch

### 7. Reverse Roles
- Let your colleague practice the same steps on your repository

---

## Step 3 – GitHub Flow (Pair Work)

### GitHub Flow Workflow

```
'master' branch
     │
     ├── create branch ──► commit changes ──► Pull Request ──► get feedback ──► test changes ──► merge branch
     │                                                                                              │
     └──────────────────────────────────────────────────────────────────────────────────────────────┘
```

### Practice the GitHub Flow

1. **Create a Feature Branch** from the main (master) branch
   ```bash
   git checkout -b feature/<your_name>/<feature_name>
   ```

2. **Make Several Changes** to the feature branch
   ```bash
   git add .
   git commit -m "Description of changes"
   ```

3. **Create a Pull Request (PR)** for this to the main branch
   - Ask your colleague to review it

4. **Review and Accept**
   - If the PR is acceptable, the colleague will accept it

5. **Delete the Feature Branch** once it's accepted
   ```bash
   git branch -d <branch_name>
   ```

6. **Reverse Roles** and let your colleague practice too

---

## Quick Reference Commands

| Command | Description |
|---------|-------------|
| `git clone <url>` | Clone a repository |
| `git branch <name>` | Create a new branch |
| `git checkout <branch>` | Switch to a branch |
| `git checkout -b <name>` | Create and switch to a new branch |
| `git add .` | Stage all changes |
| `git commit -m "message"` | Commit staged changes |
| `git push origin <branch>` | Push branch to remote |
| `git pull` | Pull latest changes from remote |
| `git branch -d <name>` | Delete a local branch |

---

## References

1. [Git Reference - Git Official Documentation](https://git-scm.com/docs)
2. [GitHub Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
