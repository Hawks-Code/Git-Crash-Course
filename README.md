# Git Crash Course

## What is Git?
![Git Logo](https://git-scm.com/images/logo@2x.png)

"Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency."

It's a tool used to track and organize code changes, typically across a team of people, that makes it easy to work on multiple parts simultaneously. 

## Git vs. GitHub
![Git vs GitHub image](https://www.simplilearn.com/ice9/free_resources_article_thumb/git_vs_github2.jpg)

**Git** - is a command line application (with optional GUI) that runs on your local computer. It tracks the changes you make to project files, stores and organizes your changes across local branches, and bundles your changes so they can be shared (push-ed) and retrieved (pull-ed) from a server (repository).

**GitHub** - cloud service and accompanying website that hosts code repositories so others can view and share them. Handles authorization for who can view/edit the code. Free for individuals, even private repositories, but advanced collaboration features are paid, public repos get a lot of advanced features free.

## Setup
### Git CLI Install
Check if you already have git installed, in a terminal run: `git -v` If that outputs a version number you already have git!

If not download and install it: https://git-scm.com/downloads

### Git Credentials Manager Install
[Git Credentials Manager](https://github.com/git-ecosystem/git-credential-manager?tab=readme-ov-file) makes authenticating with GitHub much easier, it will pull up a website to have you sign in when needed for various git actions. Once installed it just works in the background with normal git commands.

Install Instructions: https://github.com/git-ecosystem/git-credential-manager/blob/release/docs/install.md


## Basic Usage
### Clone Repo
Copy the URL for the repo you wish to clone (download to your computer):

Open the GitHub page for the repo you want to clone, like this repo: https://github.com/Hawks-Code/Git-Crash-Course

![image](https://drive.google.com/uc?export=view&id=1ewnJ-T4IkxMIQ3DVXTTUL0vwlbjImD-z)

Navigate to where you want to download the project. If you are unsure a folder in your home directory is a good place to start! (assuming unix/powershell)

```cd ~/``` navigate to home directory, appreviated ~/

```mkdir workspace``` create folder to manage coding projects in home dir.

```cd workspace``` open newly created folder.

```git clone https://github.com/Hawks-Code/Git-Crash-Course.git``` paste the URL after the command ```git clone``` to download the repo from GitHub.

```cd Git-Crash-Course``` open the cloned project and start coding!


### TODO: Make a Change
### TODO: Commit a Change
### TODO: Push a Change

## Committing to Hawks Code
### TODO: How to Pull Request
