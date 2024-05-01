# Git and Github

### Version control system
Version control system also known as source control, is tracking and managing software code changes.

#### For example

- Day 1

```
    const name = "Ankush"
```

- Day 2

```
    const name = "Ankush"
    const age = 21
```

- Day 3

```
    const name = "Ankush"
    const age = 21

    function getAge() {
        return Age;
    }
```

Now there is a bug in the day 3 code so, if you want you can also revert the code from day 3 to day 2. 

### Setup 

- Globally configuring user information

```
    git config --global user.name "Your Name"
    git config --global user.email "Your Email"
```

- if you want to check whether the given details are set or not then use following command:

```
    git config --global --list
```

OR

```
    git config --global user.name 
    git config --global user.email 
```

- Initialize a new repository by using following command inside the project.

```
    git init
```

- After initializing git in your project there is `.git` folder created in your root directory. It is hidden folder and we need to show it. Select View > Options > Change folder and search options. Select the View tab and, in Advanced settings, select Show hidden files, folders, and drives and OK.

- If you closely see your code files then you will notice that it's showing as untracked files. 

- To track your untracked file your need to write this command.

```
    git add <filename>
```

Now, whatever file name you had written instead of `<filename>` it will start tracking that particular file.

- To  add all the changes at once into staging area use this command: 

```
    git add .
```

- When you change anything in your code add or delete you can see that also by using this command: 

```
    git diff
```

- If you want to save your changes to a project's history use this command: 

```
    git commit -m "description about your changes"
```

- To display all the commit that have been made till now use this command :

```
    git log
```

 OR

```
    git log --oneline
```
Every commit is having a unique id and day/time when it was committed. 

- If you want to detailed information about any specific code commit then use following command:

```
    git show [id]
```

- This command display information about who last modified each line of a file in a Git repository, along with the commit information for each change. 

```
    git blame <filename>
```

### Staging Area

Before committing your changes to the repository, you can selectively choose which changes you want to include in the next commit by staging them. When you stage changes, you're essentially preparing them to be saved in the next commit. The staging area acts as a snapshot of what will be included in the next commit.

### Reverting Back

#### First way to revert back
- If you accidentally added something which should not be there in repository, You can remove those using below commands.

```
    git reset --hard [id]
```

After reverting use `git push -f` to force update in remote repository.

This command will make your local repo look exactly like the repository at given [id]. So, if [id] is a branch name, HEAD will be moved.

#### One more way to revert back

```
    git revert [id]
```


#### Branching in git

- A branch is simply a new line of development that can be created from the master branch. It allows developers to work on features independently without affecting.
- A branch is like a separate line of development within the project history. You can create a new branch using below command :

```
    git branch <branch name>
```

- To change your current branch use this command: 

```
    git checkout <branch name>
```

- The above to commands can be used together like so:

```
    git checkout -b <new branch name>   
```
Created a new branch and switched to it at the same time.

- To push your branch on remote server use this command: 

```
    git push --set-upstream origin <branch name>
```

We are using this command because you created the new branch from local machine and now you want to push  it into remote repo so that other can see.

#### Merging Branches

Merging is the process of integrating changes from one branch into another. In Git, you can merge any number of branches together using the following command:

```
    git merge origin / <branch name>
```

#### If you remotely merging two branches then pull the changes from a remote repo and merge it with your local one by using this command: 

```
    git pull
```