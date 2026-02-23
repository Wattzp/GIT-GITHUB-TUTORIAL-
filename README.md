# GIT AND GITHUB

### WHAT IS GIT?

Git is a **distributed version control system** designed to help developers track changes in their code, collaborate with others, and maintain a history of their projects. Here’s a clear breakdown:

### 🔑 Key Features of Git

- **Version Tracking:** Records snapshots of your project over time, so you can revisit or roll back to earlier versions.

- **Branching & Merging:** Lets you create separate branches to experiment or develop features independently, then merge them back into the main project.

- **Collaboration:** Multiple developers can work on the same project without overwriting each other’s work.

- **Distributed System:** Every developer has a full copy of the repository, including its history, on their local machine.

- **Speed & Efficiency:** Git is optimized for performance, making operations like commits, diffs, and merges very fast.

### HOW TO INSTALL GIT

To install Git, download the installer for your operating system (Windows, macOS, or Linux), run it, and then verify the installation by typing git --version in your terminal or command prompt. On macOS and most Linux distributions, Git may already be preinstalled.

🖥️ Step-by-Step Installation Guide

1. Check if Git is Already Installed
- Open Terminal (macOS/Linux) or Command Prompt/Git Bash (Windows).

- Run:

`git --version`

- If Git is installed, you’ll see the version number. If not, proceed with installation.

2. Windows Installation
Download: Go to the official Git website and download the latest Windows installer.

Run Installer: Double-click the .exe file and follow the setup wizard.

Recommended: Accept default options unless you have specific needs.
Verify: Open Command Prompt or PowerShell and run:

git --version

Official Git web site: [GIT](https://www.git-scm.com/)

Official GitHub.com web site: [GITHUB](https://github.com/)

### 🛠️ HOW GIT IS USED
- **Local Development:** Developers commit changes to their local repository.

- **Remote Collaboration:** Teams often use platforms like GitHub, GitLab, or Bitbucket to share repositories online.

- **Project Management:** Git helps organize workflows, track bugs, and manage releases.

#### Example Workflow
- **Clone** a repository (download a copy).

- **Create** a branch for a new feature.

- **Commit** changes as you work.

- **Merge** your branch back into the main project.

- **Push** updates to a remote repository so others can access them.

**NOTE** When you install GIT, it comes with a terminal called GIT BASH. To launch it, simply click on your start menu and then type in git bash and then you can launch it. But you can also use any other terminal that you have on your computer. You can also use PowerShell, Command prompt. If you are on Mac, you could use the terminal that comes with your machine.

First configure your name and your email. This is important so that anytime we commit something or write something to the history book, we need to know who is doing it.
We specify the name using: 

`git config --global user.name "your name"` then press `Enter`.

We specify the email using:

`git config --global user.email "your email"` then press `Enter`.

We might also want to specify the default branch name, this might not make not make much sense now, but there are other branches that we would put in place later. 

`git config --global init.default branch main` then press `Enter`. # init.default == initialize.default.
    To change your default branch in Git from master to main using Git Bash, you’ll need to update both your local repository and the remote repository (e.g., GitHub).
    
**Local Repository Steps**
1. Rename the branch locally:
    `git branch -m master main`. This renames your current branch from `master` to `main`.
2. Update the upstream tracking branch:
    `git fetch origin`
    `git branch -u origin/main main`. This ensures your local `main` branch tracks the remote `main`.
3. Set HEAD to point to main:
    `git symbolic-ref refs/remotes/origin/HEAD refs/remotes/origin/main`.

**Remote Repository (GitHub/GitLab)**
1. Push the renamed branch:
    `git push -u origin main`
2. On GitHub (or your remote host), go to Repository Settings → Branches and set main as the default branch.
3. Optionally, delete the old `master` branch from the remote:
    `git push origin --delete master`

### SOME COMMAND PROMPT IN GIT CONFIG
To access other commands in git use:

`git config -h` then press `Enter`. This shows the **help information** for the `git config` command. This includes:

- __Options and flags__:

- `--global` → Apply settings for your user account across all repositories.

- `--system` → Apply settings system-wide.

- `--local` → Apply settings only to the current repository.

- `--list` → Show all current configuration settings.

- `--get <name>` → Retrieve the value of a specific configuration variable.

- `--unset <name>` → Remove a configuration variable.

- `--edit` → Open the configuration file in your default editor.

We can also see other detailed information on `git config` by running:

`git help config` then press `Enter`. This open up a manual that is hosted on your computer so even if you don't have internet access you can still be able to access this file.

To clear your termial and start afresh, simply type **`Clear`** and press `Enter`

#### CHANGE THE DIRECTORY 
1. If you want to commit in a different folder/repository

- Navigate to that folder in the Git Bash:

cd path/to/your/repo
Example:
cd C:/Users/Vincent/Downloads

Then to turn this to a Git repisitory you use:
`git init` 
then press `Enter`
This initializes our repository in our directory.
Check your file directory, you'll see a new `.git` folder. Once you click on `.git` you'll see all your necessary repository files. 

2. Still in your `GIT BASH` Terminal:
   type in `git status` this will tell you the status of your repository i.e it shows:
   - the branch of your repository(main/master)
   - the number of commit made
   - the untracked files; files in your file explorer (currently all files will be untracked meaning that if I make any changes to this files `Git` won't recognized it because they're untracked. But if I track a file `Git` would know what changes I made to the file.
  
To track a file I simply type in `git add` and then I could specify the file name. For example:
`git add the name of the file` then click `enter`
To cofirm the file is now been tracked, type in `git status`
To untrack a file back simple use: `git rm-- cached <file>`.

  To ignore or hide a file from git to see it from your file explorer, you go to your files in your file explorer and then add a new text document called `.gitignore`. This allows us to ignore certain files,folders, or even entire extension. Rename your text document `.gitignore`, a pop-up will appear idicating "It might become unstable if you also change the file extension. `.txt`, click on yes. A new file `.gitignore` is then created. 
Open it and it opens as a notepad. Here you can tell git what files to ignore. 
Example you can commit using "# ignore all .txt files, underneath it you can type in an asterisk, *, so basically any filename.txt, will be ignored, then go to file and save. 
  To see a comprehensive list of all the different files,folders, or even just an entire extensions, you can go to https://github.com/github/gitignore. This are important to log files, auto generated files or any files that you don't want to include as part of your project.
Back in git bash, type in `git status` and you'll no longer see those files you ignore.

Remember we tracked only one file before, "index.htm", but then we also untracked it so its back to our stagged files to be committed.

To track all files at once,
type:  `git add --all` alternatively `git add --A` or simply `git add .` then once again press `enter`. 
then once again type your `git status`, here you see all the files are currently been tracked tracked except for the file that I  ignored, and currently all these files are in an environment called **Staging** 
















