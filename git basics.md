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

#### The lifecycle of the status of your files
![image](https://github.com/user-attachments/assets/08763e5e-73f9-4a81-8340-8820e5e398d2)

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
