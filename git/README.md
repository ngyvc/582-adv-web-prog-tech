# Git

## Top Tips

- If you aren't sure about a git move, create a new branch (Branches are free!)
- You can have as many branches as you want and switch between them before merging
- You can always delete backup branches or do cleanup later

## Introduction to Git

### Essential links

- [Git and GitHub for Beginners - Crash Course](https://www.youtube.com/watch?v=RGOj5yH7evk)

#### Using Git Locally

- [Git](https://git-scm.com/)
- [Homebrew](https://brew.sh/) (For Mac OS)

#### GitHub Signup

- [GitHub](https://github.com/)
- [Github Education Access](https://education.github.com/)
- [Applying to Global Campus](https://docs.github.com/en/education/-explore-the-benefits-of-teaching-and-learning-with-github-education/github-global-campus-for-students/apply-to-github-global-campus-as-a-student)

#### GitHub Copilot

- [Github Copilot](https://github.com/features/copilot)
- [GitHub Copilot Billing for Education](https://docs.github.com/en/billing/-managing-billing-for-github-copilot/-about-billing-for-github-copilot#pricing-for-github-copilot-for-individuals)
- [GitHub Copilot Quickstart](https://docs.github.com/en/copilot/quickstart)

#### Github Shortcuts

- Use the . (period) key to change github repo view to developer mode
- [Keyboard shortcuts](https://docs.github.com/en/get-started/using-github/keyboard-shortcuts)
- [The github.dev web-based editor](https://docs.github.com/en/codespaces/the-githubdev-web-based-editor)

#### Git for Plesk

- [Git for Plesk](https://www.plesk.com/extensions/git/)

### Why use Git?

- History tracking
- Multi version of a project
- Multi branch code sharing and teamwork

### Version control

- Subversion control
- Distributed control

### Advantages, disadvantages & Myths

- Free and unlimited branching
- Access - locked vs shared - team leader
- Git is too heavy with all the history
- Bad for binary files - images, videos
- Not as user friendly
- Hard to understand, but easy to use

### Running Commands

#### Apps

- Commend prompt
- powershell
- terminal
- iTerm

#### Commands

- pwd (print working directory)
- cd (change directory)
- ls / dir (listing / directory)
- touch / copy con (new file)
- mkdir (make directory)

### Git Configuration

```git
git —version
git config —global user.name "name"
git config —global user.email "email"
git config —list
```

Remove —global for local settings

```git
man git (git manual, use :q to quit)
```

### Stages of a file

- Untracked
- Committed
- Modified
- Staged
- Add

(Working directory - staging area (index) - .git directory)

### Git introduction

```git
git init
git add
git commit
git commit -m "message"
git comment -am "message"
git log --oneline
git branch
```

```git
git checkout
git rebase
git merge
git diff
```

```git
git checkout -b new-branch
git switch
git branch -d
```

### Rebase Branches

```git
git swtich branch
git rebase main
git reflog
git pull --rebase
```

### Merging Branches

```git
git diff branch1 branch2
```

```git
git checkout target
git merge source
```

ex:

```git
git checkout main
git merge feature/js
```

### Cloning remote

```git
git clone remote-url
git remote -v
git remote update
git fetch
git pull
git push
```

```git
git ls-remote
git push -u origin new-branch
git fetch original new-branch
git branch -a
git checkout --track origin/new-branch
```

### PR - Pull Request

- use PR for reviews and approval of updates

[Creating a pull request from a fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)

[Syncing a fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork)

### Cherry pick

```git
git cherry-pick SHA
```

### GitHub

- Hosting service
- Management tools
- Social network on coding
- Workflow

### PR (Pull request) workflow

- Fork to clone project inside GitHub
- Submit commits
- PR to original

### Intentionally untrack using .gitignore

[.gitignore](https://git-scm.com/docs/gitignore)
[.gitignore templates](https://github.com/github/gitignore/tree/main)
[.gitignore template for Node](https://github.com/github/gitignore/blob/main/Node.gitignore)

## Exercises

### Basic

- Create a page and commit changes as you add new section or content

### Intermediate

- Fork my demo repo
- PR
- Commit, diff, rebase

### Advanced

- Create a project with another classmate
- Split a page creation to your teammate
- PR
- Commit, diff, rebase
