Git is a distributed version control system designed to handle everything from small to very large projects with speed and efficiency. It allows multiple developers to work on a project simultaneously without overwriting each other's changes. It keeps a complete history of changes, which can be reviewed and rolled back if necessary.

### Key Concepts of Git:
1. **Repository (Repo)**: A directory where Git stores all of its tracked files and their history.
2. **Branch**: A pointer to a specific commit. Multiple branches allow developers to work on different features or fixes without disturbing the main project.
3. **Commit**: A snapshot of your code at a particular point in time, along with a message explaining what changes were made.
4. **Merge**: Combining changes from different branches.
5. **Pull/Push**: Pull fetches the latest changes from a remote repository and applies them to your local repository. Push uploads your local changes to a remote repository.
6. **Clone**: Create a local copy of a remote repository.
7. **Stage/Unstage**: Staging is the process of selecting changes to include in the next commit. Unstaging removes those changes from the stage.

### Installation and Configuration:
1. **Installation**: 
    - On Linux: Use your package manager, e.g., `sudo apt install git` on Debian or Ubuntu.
    - On macOS: Install Xcode from the App Store or download the console tools from the [Apple Developer Resources Page](https://developer.apple.com/xcode/resources/)
    - On Windows: Download from the [official Git site](https://git-scm.com/downloads).
2. **Initial Configuration**: After installing Git, configure it globally using the following commands:
```bash
    git config --global user.name "Your Name"
    git config --global user.email "youremail@example.com"
```
These set your identity for commits.

2. **Other Useful Configurations**:
    - **Default text editor:**
```bash
    git config --global core.editor 'code'  # Or use vim, nano, etc.
```
    - **Set line endings (useful for cross-platform projects):**
```bash
    git config --global core.autocrlf true  # For Windows 
    git config --global core.autocrlf input # For macOS/Linux`
```
3. **Verify the Configuration**: To check your Git configuration, use:
```bash
    git config --list
```

### Basic Git Workflow:
1. **Create a New Repository**: 
    - To initialize a new repository in your project directory:
```bash
    git init
```

2. **Clone an Existing Repository**: 
    - To clone a remote repository:
```bash
    git clone <repository_url>
```

3. **Check Repository Status**:
    - To see the status of your files (e.g., modified, staged, etc.):
```bash
    git status
```

4. **Stage Files for Commit**:
    - Stage specific files:
```bash
    git add <file_name>
```
    - Stage all changed files:
```bash
    git add . 
```    
      or with files in subfolders
```bash
    git add `find . type f`
```

5. **Commit Changes**: 
    - Commit staged changes with a message:
```bash
    git commit -m "Describe what you changed"
```

6. **View Commit History**:
    - To see the commit history:
```bash
    git log
```

7. **Create and Switch Branches**:
    - Create a new branch:
```bash
    git branch <branch_name>
```
    - Switch to an existing branch:
```bash
    git checkout <branch_name>
```
8. **Merge Branches**:
    - Merge changes from one branch into another (while on the branch you want to merge into):
```bash
    git merge <branch_name>
```
9. **Push and Pull from Remote Repositories**:
    - Push your local commits to a remote repository:
```bash
    git push origin <branch_name>
```
    - Pull changes from the remote repository:
```bash
    git pull origin <branch_name>
```

10. **Handling Conflicts**:
    - Sometimes, Git will warn you about conflicts when merging branches or pulling changes. You will need to manually resolve these conflicts, usually by editing the affected files and then staging and committing the resolved versions.

### Useful Git Commands:
1. **Undo Changes**:
    - Unstage a file (before committing):
```bash
    git reset <file_name>
```
    - Undo local changes (before staging):
```bash
    git checkout -- <file_name>
```

2. **Delete a Branch**:
    - Delete a local branch:
```bash
    git branch -d <branch_name>
```
    - Delete a remote branch:
```bash
    git push origin --delete <branch_name>
```
        
3. **Stash Changes**:
    - Temporarily store your changes and clean your working directory:
```bash
    git stash
```
    - Apply stashed changes later:
```bash
    git stash apply
```
4. **Tagging**:
    - Create a tag for a release or milestone:
```bash
    git tag <tag_name>
```

### Working with Remote Repositories:
1. **Adding a Remote Repository**:
    - To add a remote repository:
```bash
    git remote add origin <repository_url>
```
2. **Fetch Changes**:
    - Fetch new changes from the remote without merging:
```bash
    git fetch
```
3. **Tracking Branches**:
    - If you want to set the default remote branch to push/pull from:
```bash
    git branch --set-upstream-to=origin/<branch_name>
```

With these basics, you can start managing your code effectively using Git.

## .gitignore

A **.gitignore file** tailored for a web application development environment using Visual Studio Code, HTML, CSS, JavaScript, Node.js, MongoDB, and PostgreSQL:
```
## .gitignore for web application development 
## Visual Studio Code and Node.js, MongoDB, and PostgreSQL
## RGoe 2024.10.16 - V.:0.00
## Logs
logs
*.log
npm-debug.log*
yarn-debug.log*
yarn-error.log*

## Node.js specific
node_modules/
npm-debug.log
yarn-debug.log
.pnpm-debug.log
.cache/
dist/
build/
.temp/

## MongoDB
data/db/
*.lock
mongod.lock

## PostgreSQL
pgdata/
*.pid
*.log

## Environment variables
.env
.env.local
.env.*.local

## Visual Studio Code
.vscode/
*.code-workspace
.vscode-test/

## IDE-specific
.idea/
*.suo
*.ntvs*
*.njsproj
*.sln
*.sw?

## Dependency directories
jspm_packages/
bower_components/

## Optional npm cache directory
.npm

## Optional eslint cache
.eslintcache

## Optional stylelint cache
.stylelintcache

## TypeScript specific
*.tsbuildinfo

## Test Coverage
coverage/

## Parcel-bundler cache (if used)
.cache/

## Next.js build output (if applicable)
.next/
out/

## Nuxt.js build output (if applicable)
.nuxt/
dist/

## Gatsby files (if applicable)
.cache/
public/

# Vuepress build output (if applicable)
.vuepress/dist

## SvelteKit build output (if applicable)
.svelte-kit/

## Gridsome (Vue.js framework) build output
dist/
static/

## Static site generators
public/

## Prettier formatter log files
.prettier-cache

## Build artifacts
*.js.map
*.css.map

## Temporary files
*.tmp
*.temp
*.bak
*.swp
*.swo

## SASS Cache
.sass-cache/

## Coverage and linting results
coverage/
.lcov/
*.lcov
*.log
*.out
*.test

## OS generated files
## Linux files
*~ 
.nfs*

## MacOS metadata
.DS_Store
.AppleDouble
.LSOverride

## Windows files
Thumbs.db
ehthumbs.db

## Miscellaneous
*.pid
*.seed
*.pid.lock
*.envrc
*.pnp.js
.pnp/

## Local project settings
*.local

## EOF .gitignore
```

# Resources 
* [Download Git Software](https://git-scm.com/downloads)
* [Git Documentation Book - Pro Git](https://git-scm.com/book/en/v2)
* [Git Documentation Videos](https://git-scm.com/videos)
* **[Git Reference](https://git-scm.com/docs)**
* [Git Cheat sheet](https://ndpsoftware.com/git-cheatsheet.html#loc=index;)

* [More Git Resources](https://git-scm.com/doc/ext)

## [Getting Started with git](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)

```console
$ git init
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
$ git config user.name
$ git branch -m master main
$ git add index.html
$ git commit -m "initial commit"
$ git status
$ git log
$ git checkout ...
$ git checkout main
$ git branch feature/header
$ git branch
$ git checkout feature/header
$ git commit 
$ git checkout main
$ git merge feature/header
$ git commit
$ `git checkout -b feature/fix-issue
```




