GitHub is an online platform that provides hosting for software development and version control using [Git](Web-Application-Development-Docu/Tools/VCS/Git). It is a collaborative platform where developers can share their code, work on projects together, track changes, and contribute to open-source software. GitHub offers several features, including issue tracking, project management tools, and continuous integration (CI) workflows, making it highly versatile for both individual developers and teams.

### Key Features of GitHub:

1. **Repository Hosting:** GitHub hosts Git repositories, where developers store their code. Repositories (or repos) can be public, allowing anyone to view or contribute to them, or private for controlled access.
    
2. **Version Control with Git:** Git is a distributed version control system that tracks changes in code over time. This allows developers to maintain different versions (branches) of their code, collaborate on features, and merge changes back into the main project.
    
3. **Collaboration Tools:** GitHub makes it easy for multiple developers to work together. They can submit changes to the codebase through pull requests, allowing maintainers to review, discuss, and merge updates into the main branch.
    
4. **Issue Tracking:** GitHub provides a built-in issue tracker for bugs, feature requests, or general discussions, helping teams stay organized.
    
5. **GitHub Pages:** It can be used to host websites directly from a GitHub repository, making it ideal for project documentation or personal portfolio sites.
    
6. **CI/CD Integration:** GitHub can be integrated with continuous integration/continuous deployment (CI/CD) tools to automate testing and deployment.
### Basic Git Commands:
- **`git clone <repository_url>`**: Downloads a copy of a GitHub repository to your local machine.
- **`git status`**: Shows the current state of your working directory and staging area.
- **`git add <file>`**: Stages changes to be committed.
- **`git commit -m "message"`**: Records the staged changes to the repository.
- **`git push`**: Sends the committed changes to a remote repository (like GitHub).

### Before you begin GitHub SSH setup:

By default, Git communicates with GitHub over HTTPS. However, for enhanced security and ease of use, many developers prefer to set up SSH keys to authenticate with GitHub. When using SSH, you don’t need to enter your GitHub username and password every time you push changes.

Here’s how to set up GitHub to use SSH for `git push`:

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

---
## Resources
* [# Download GitHub Desktop](https://desktop.github.com/download/) and [# GitHub Desktop Documentation](https://docs.github.com/en/desktop/installing-and-authenticating-to-github-desktop/installing-github-desktop)
* [# GitHub Training Kit](https://training.github.com/)
* 