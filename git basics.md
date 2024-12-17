## Getting a Git repository
1. You can take a local directory that is currently not under version control, and turn it into a Git repository, or
2. You can clone an existing Git repository from elsewhere.
### Initializing a Repository in an Existing Directory
If you have a project directory that is currently not under version control and you want to start controlling it with Git, you first need to go to that project’s directory.

and type:  ```git init```

Helpful commands
```git status```

if you want to add a file (i.e. file.txt) for snapshots and saving the changes, you can run: ```git add file.txt```

### Cloning an Existing Repository
If you want to get a copy of an existing Git repository — for example, a project you’d like to contribute to — the command you need is git clone.

You clone a repository with git clone . For example, if you want to clone the Git linkable library called libgit2, you can do so like this:

```$ git clone https://github.com/libgit2/libgit2```

But, make sure you first cd to the directory that you want to clone.

#### Three main sections of a Git project 
Working tree, staging area, and Git directory
![image](https://github.com/user-attachments/assets/cc99537b-82bd-46fd-96fe-8362c064691a)

## Recording Changes to the Repository

#### The lifecycle of the status of your files
![image](https://github.com/user-attachments/assets/08763e5e-73f9-4a81-8340-8820e5e398d2)

#### Please note

Each file in a Git repository can be in one of two main states: tracked or untracked.

● 1. Tracked files: are files that Git is aware of because they were either in the last snapshot of the repository or have been newly staged, meaning they have been marked to be included in the next snapshot. The last snapshot is located in the Git directory. These files can be further classified as unmodified, modified, or staged:

○ Unmodified: The file hasn't changed since the last commit.

○ Modified: If you modify a tracked file, it becomes modified. The file has been changed since the last commit. You can stage the modified file using ```git add <filename>``` to include it in the next commit.

○ Staged: You use ```git add <filename>``` to begin tracking the modified file, which moves it to the staged state. This will mark it to be included in the next snapshot or commit. 

● 2. Untracked files: Any file that is created is initially untracked. They are within the working directory that Git doesn't know about them because they were not present in the last snapshot and aren't in the staging area. When you clone a repository for the first time, all files are tracked and unmodified because Git just checked them out, and you haven't changed anything yet. As you begin to edit files, they become modified.


### Checking the Status of Your Files
The main tool you use to determine which files are in which state is the git status command.

```$ git status```

### Tracking New Files
In order to begin tracking a new file, you use the command ```git add```.
```$ git add README```
### Short Status
Git also has a short status flag so you can see your changes in a more compact way. If you run ```git status -s``` or ```git status --short``` you get a far more simplified output from the command:
```$ git status -s```
New files that aren’t tracked have a ```??``` next to them

## Ignoring files
For a list of patterns that can be used in ```.gitignore``` files, you can check the following:

https://git-scm.com/docs/gitignore#_pattern_format

this link or Atlassian gitignore guide.
