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

