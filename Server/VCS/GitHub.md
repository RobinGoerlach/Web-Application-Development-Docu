GitHub is an online platform that provides hosting for software development and version control using [Git](Web-Application-Development-Docu/Tools/VCS/Git). It is a collaborative platform where developers can share their code, work on projects together, track changes, and contribute to open-source software. GitHub offers several features, including issue tracking, project management tools, and continuous integration (CI) workflows, making it highly versatile for both individual developers and teams.

## Key Features of GitHub:
1. **Repository Hosting:** GitHub hosts Git repositories, where developers store their code. Repositories (or repos) can be public, allowing anyone to view or contribute to them, or private for controlled access.
2. **Version Control with Git:** Git is a distributed version control system that tracks changes in code over time. This allows developers to maintain different versions (branches) of their code, collaborate on features, and merge changes back into the main project.
3. **Collaboration Tools:** GitHub makes it easy for multiple developers to work together. They can submit changes to the codebase through pull requests, allowing maintainers to review, discuss, and merge updates into the main branch.
4. **Issue Tracking:** GitHub provides a built-in issue tracker for bugs, feature requests, or general discussions, helping teams stay organized.
5. **GitHub Pages:** It can be used to host websites directly from a GitHub repository, making it ideal for project documentation or personal portfolio sites.
6. **CI/CD Integration:** GitHub can be integrated with continuous integration/continuous deployment (CI/CD) tools to automate testing and deployment.
## Basic Git Commands:
- **`git clone <repository_url>`**: Downloads a copy of a GitHub repository to your local machine.
- **`git status`**: Shows the current state of your working directory and staging area.
- **`git add <file>`**: Stages changes to be committed.
- **`git commit -m "message"`**: Records the staged changes to the repository.
- **`git push`**: Sends the committed changes to a remote repository (like GitHub).
See more in [Git...](Web-Application-Development-Docu/Tools/VCS/Git)

### Before you begin GitHub SSH setup:
By default, Git communicates with GitHub over HTTPS. However, for enhanced security and ease of use, many developers prefer to set up SSH keys to authenticate with GitHub. When using SSH, you don’t need to enter your GitHub username and password every time you push changes.
#### 1. **Generate SSH Key**:
If you don't already have an SSH key, you can generate one using the following command in your terminal:
`ssh-keygen -t ed25519 -C "your_email@example.com"`

This will create an SSH key pair, with the private key stored on your computer and the public key to be added to your GitHub account.
#### 2. **Add SSH Key to GitHub**:
- Copy the contents of your public key file, usually found in `~/.ssh/id_ed25519.pub` (or a similar location if using a different algorithm):
`cat ~/.ssh/id_ed25519.pub`
- Go to GitHub, and in your profile settings, find **SSH and GPG keys**. Add your new SSH key by pasting the public key.
#### 3. **Test SSH Connection**:
After adding the key to GitHub, test the SSH connection to ensure everything is working:
`ssh -T git@github.com`
You should see a message confirming that the SSH connection to GitHub is successful.
#### 4. **Use SSH for Git Operations**:
When cloning or working with repositories, use the SSH URL instead of HTTPS. You can find this option on the repository page on GitHub:
`git clone git@github.com:username/repository.git`

Now, when you run `git push`, Git will use your SSH key for authentication, and you won’t need to enter your credentials.
This setup streamlines your workflow and improves security by eliminating the need for manual login every time you interact with your repository.

## **Creating a new repository on GitHub**
Creating a new repository on GitHub after logging in is straightforward. Here's a step-by-step guide to help you through the process:
### Step-by-Step: Creating a New GitHub Repository
#### 1. **Log in to GitHub**
First, ensure you're logged into your GitHub account by visiting [GitHub.com](https://github.com).

#### 2. **Go to Repositories Section**
- Once logged in, in the top right corner, click on your profile picture or avatar.
- From the dropdown menu, select **Your repositories**.

#### 3. **Click on the "New" Button**
- On the repositories page, you will see a green **"New"** button to create a new repository. Alternatively, you can directly navigate to [github.com/new](https://github.com/new).

#### 4. **Fill in Repository Details**
Now you'll be taken to a page where you can enter the details for your new repository:
- **Repository Name:** Enter a unique name for your repository. This will be the main identifier for your project.
- **Description (Optional):** You can add a short description of the project to help others understand what it's about.
- **Visibility:**
    - **Public:** Anyone on GitHub can view your repository.
    - **Private:** Only you (and anyone you invite) can view and access the repository.

#### 5. **Initialize the Repository (Optional, but recommended)**
GitHub provides options to initialize your repository with useful files:

- **Add a README file:** This file is a markdown document where you can describe your project. It’s usually the first file others see when they visit your repository.
- **Add .gitignore:** Select a template that specifies which files Git should ignore. This is useful for excluding unnecessary files, like system or dependency files, from your version control.
- **Choose a license:** If you're creating an open-source project, GitHub offers several open-source license options (like MIT or GPL). Adding a license informs others of how they can use and contribute to your code.

#### 6. **Create the Repository**
After filling out all the necessary information, click the **"Create repository"** button at the bottom of the page. This will create your new repository.

#### 7. **Connect Your Local Machine to the Repository (Optional)**
If you plan to work on this repository locally (on your computer), you can follow the instructions that GitHub provides after the repository is created. You’ll see options for:
- **Create a new repository on the command line**

```bash
    echo "# your-new-repo" >> README.md git init git add README.md 
    git commit -m "first commit" 
    git branch -M main git remote add origin git@github.com:username/new-repo.git 
    git push -u origin main
```
    
- **Push an existing repository from the command line**:
    
```bash
    git remote add origin git@github.com:username/new-repo.git 
    git branch -M main git push -u origin main
```

### Step-by-Step: Pushing Changes to GitHub with SSH
If you’ve already set up SSH (as discussed earlier), you can push changes from your local machine to the new repository without needing to enter credentials each time.

1. **Navigate to Your Project Directory**: Open a terminal on your local machine and navigate to the directory where your project is stored: 
```bash
    cd /path/to/your/project
```
    
2. **Initialize Git (If not already done)**: If your project isn’t already a Git repository, initialize Git with the following command: 
```bash
    git init
```

3. **Add Remote Repository**: Add the newly created GitHub repository as the remote origin (replace the URL with your actual repository URL):
```bash
    git remote add origin git@github.com:username/new-repo.git
```    

4. **Stage and Commit Your Changes**: Add your project files and commit them to the local repository:
```bash
    git add . git commit -m "Initial commit"
```    

5. **Push to GitHub**: Push the changes to the GitHub repository:
```bash
    git push -u origin main
```
    This will push your local project to GitHub’s `main` branch, making it accessible online.

Your repository is now created, and your code is pushed to GitHub! You can continue collaborating on this project, managing its versions, and inviting others to contribute.
---
## Resources
* [# Download GitHub Desktop](https://desktop.github.com/download/) and [# GitHub Desktop Documentation](https://docs.github.com/en/desktop/installing-and-authenticating-to-github-desktop/installing-github-desktop)
* [# GitHub Training Kit](https://training.github.com/)
 
