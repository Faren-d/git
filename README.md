# Git


The book: Pro git

https://git-scm.com/book/en/v2


## Git vs. Github

Git and GitHub are not the same thing. Git is an open-source, version control tool created in 2005 by developers working on the Linux operating system; GitHub is a company founded in 2008 that makes tools which integrate with git. You do not need GitHub to use git, but you cannot use GitHub without using git. There are many other alternatives to GitHub, such as GitLab, BitBucket, and “host-your-own” solutions such as gogs and gittea. All of these are referred to in git-speak as “remotes”, and all are completely optional. You do not need to use a remote to use git, but it will make sharing your code with others easier.

There are many git hosting providers, such as github

## Vscode
To make a folder and open the vscode from terminal, follow these steps:

```mkdir tmp-git-practice```

```cd tmp-git-practice```

``` code .```

In Vscode, install the extension 'remote-wsl' if you use wsl

## Extensions

There are literally thousands of extensions in the VS Code marketplace with new ones coming seemingly every single day!

Extensions are really important to customizing your software to suit your personal needs. So please use them!

For Git we will use the following extensions:

- Git Graph: https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph

- Git Lens: https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens

We highly recommend you to install the following extensions as well for a better theme (this is a personal preference and completely optional):

- Material Theme Icons

- Material Theme

- Material Icon Theme

- Dark + Material


Note: The path to git config file for each level of configuration may be slightly different on your system. To check the path to the config file for global level for example, run ```git config --global --edit``` and check the opened file path. The same applies for the other levels.

## First Time Git Setup

![git-config](https://github.com/user-attachments/assets/a6d918b7-5304-4608-b9fc-e12c7842ef19)

Git comes with a tool called git config that lets you get and set configuration variables that control all aspects of how Git looks and operates. These variables can be stored in three different places:

1. [path]```/etc/gitconfig``` file: Contains values applied to every user on the system and all their repositories. If you pass the option ```--system``` to git config, it reads and writes from this file specifically. Because this is a system configuration file, you would need administrative or superuser privilege to make changes to it.

2. ```~/.gitconfig``` or``` ~/.config/git/config``` file: Values specific personally to you, the user. You can make Git read and write to this file specifically by passing the
``` --global``` option, and this affects all of the repositories you work with on your system.

3. config file in the Git directory (that is, ```.git/config```) of whatever repository you’re currently using: Specific to that single repository. You can force Git to read from and write to this file with the ```--local``` option, but that is in fact the default. Unsurprisingly, you need to be located somewhere in a Git repository for this option to work properly.

Each level overrides values in the previous level, so values in .git/config trump those in [path]/etc/gitconfig.

## Exit GNU nano in Ubuntu
ctrl+x

In order to set vscode as your editor, you need to write the following command:

```$ git config --global core.editor "code --wait"```

After that, you can open your .gitconfig file on your vscode by the following command:

```$ git config --global --edit```


### Setting Your Username and Email

It’s important to set your user name and email address because every Git commit uses this information, and it’s immutably baked into the commits you start creating:

```$ git config --global user.name "John Doe"```

```$ git config --global user.email "-----"```

### Checking Your Settings

You can check your settings at any time by running the command:

```git config --list```

If you want to see which changes related to which level, run the following command:

```$ git config --list --show-origin```

### Listing all files and directories

The ```ls -a``` command lists all files and directories in the current directory, including hidden files (those that start with a dot .). Let me break down the output you've shown:

```.``` represents the current directory
```..``` represents the parent directory
file.txt is a regular file
main.py is another regular file

The ```-a``` flag (which stands for "all") ensures that even hidden files and the . and .. directory references are displayed, unlike a standard ls command which would typically only show the regular files (file.txt and main.py).

## Getting a Git repository

1. You can take a local directory that is currently not under version control, and turn it into a Git repository, or
2. You can clone an existing Git repository from elsewhere.

### Initializing a Repository in an Existing Directory

If you have a project directory that is currently not under version control and you want to start controlling it with Git, you first need to go to that project’s directory.

and type:
``` git init```

#### Helpful commands

```git status```

if you want to add a file (i.e. file.txt) for snapshots and saving the changes, you can run: ```git add file.txt```

### Cloning an Existing Repository

If you want to get a copy of an existing Git repository — for example, a project you’d like to contribute to — the command you need is git clone.

You clone a repository with git clone <url>. For example, if you want to clone the Git linkable library called libgit2, you can do so like this:

```$ git clone https://github.com/libgit2/libgit2```

But, make sure you first ```cd``` to the directory that you want to clone.
