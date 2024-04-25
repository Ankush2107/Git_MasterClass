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

if you want to check whether the given details are set or not then use following command:

```
    git config --list
```

OR

```
    git config --global user.name 
    git config --global user.email 
```