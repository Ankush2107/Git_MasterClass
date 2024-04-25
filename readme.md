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

Now there is a bug in the day 3 code so, if you want you can also revert your code the from day 3 to day 2. 

### Setup 

- Globally configuring user information

```
    git config --global user.name "Your Name"
    git config --global user.email "Your Email"
```

- if you want to check whether the given details are set or not then use following command:

```
    git config --list
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