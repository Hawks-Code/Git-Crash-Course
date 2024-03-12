# Git Crash Course

## What is Git?
![Git Logo](https://git-scm.com/images/logo@2x.png)

"Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency."

It's a tool used to track and organize code changes, typically across a team of people, that makes it easy to work on multiple parts simultaneously. 

### Commits
A commit is a code change that has been bundled together, it can span across multiple files. It should be limited to one logical code change, eg: "add calendar to website" or "fix discord bot startup". 

Avoid waiting until the end of a project to commit everything, since then all of the code will look like it was added at once, making it hard to review and track history.

### Branches
You don't need to understand branches to get started, but this is where the real power of Git is at. Branches are variations of code used to track adding features or versions, they can be used swapped to/from if you are working on multiple features at the same time. Branches can be local (only used for organizing code you're actively working on), remote (shared across a team), or personal-remote (used as a backup/storage but not shared by a team). 

When it comes time to add a feature to the main branch of the codebase, Git helps 'merge' the two branches together intelligently based on the commits that were made in both branches. This is where you run into potential conflicts if multiple people have made conflicting changes to the same code. 

Visualization of Branches:

![git branches image](https://user-images.githubusercontent.com/1256329/80170009-f9d03200-85b4-11ea-94d3-3041887565ac.png)

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

```mkdir workspace``` create a folder to manage coding projects in home dir.

```cd workspace``` open newly created folder.

```git clone https://github.com/Hawks-Code/Git-Crash-Course.git``` paste the URL after the command ```git clone``` to download the repo from GitHub.

```cd Git-Crash-Course``` open the cloned project and start coding!


### Make a Change
Edit the project as you desire with whatever editor you like. Most IDEs will have built-in support for Git to highlight changes and make commits, but you can do everything over the command line.

You can check what files were changed by running ```git status```

```
> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

### Commit a Change
Once you have completed a code change you 'commit' it.

Run ```git status``` to see the current changed files. Note it will say these files are "not staged for commit" meaning it sees the file was changed but you need to tell Git to include changes to that file in a new commit. 

If you want to include all of the files you changed/added at once run: ```git add -A```
```
> git add -A
> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
```

**Add a useful message!**

Each commit has a string message associated with it. It should at the least include a few words describing the change made, and ideally link to further resources explaining why this change was needed.

I find the easiest way to specify the message is with the ```-m``` flag with ```git commit```, if you just run ```git commit``` on its own you will be prompted for a message in an annoying editor.

```git commit -m "updated README documentation"```

**Now you have a commit!** but it's only on your computer (on your local branch) Keep reading to 'push' your commit to GitHub.


### Push a Change

If you have full access to whatever remote repository you are trying to push to you can simply run ```git push```. However for some of the repositories the club uses commits must be reviewed by someone else in the club before they can be pushed to the **main** branch.

For that you will need to create a 'pull request'.

## Committing to Hawks Code
### TODO: How to Pull Request
