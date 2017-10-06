
# Git basics
<img src="../assets/octocat.png" />

## What's git all about?

Git is a VCS ( Version Control System ) that helps you keep track of the changes that have been made in your code.
Git thinks about it's data as more like a `stream of smapshots`.

## Installing Git on your machine

If you are using a UNIX/LINUX based operating system, `git` already comes pre-installed so you have nothing to worry about.
If you happen to have a Windows OS, you could just download it and then you're good to go.

## Basic git concepts

### Initializing Git

When we `initialize git` in a folder, what this means is that  `we want to start tracking changes that are being made` in that folder.

This is done by running the command

```$ git init ``` 

### Clone

You see a nice repository on github you like, and you want all that source code on your computer for you to do extra work ( or not ). What you need to do is to clone the repository.
Cloning a repository is no uncertain terms is `copying all the existing data from the the repository to your machine`.

This is done by running the command 

```$ git clone git@github.com:GDGLegon/code-lab.git```

In this case `git@github.com:GDGLegon/code-lab.git` is the repository we want to clone, but this can always be replaced by any repository if your interested.

### Branch

After cloning a repository, you might want to add a specific feature to the app but you don't want to break anything that already works. What is usually best in this case is to `make a new branch` where you'll implement your features and then `merge` the changes once your done.

This is done by running the command:

```$ git branch branchname```

Where `branchname` is the name of the new branch you want to create

To see all exisiting branches in the repository you do this:

```$ git branch```

Keep in mind, we only created this new branch , we are not inside the branch yet
To jump into your new branch, you run this command:

```$ git checkout branchname```

To delete a branch you no longer need, you run this command:

```$ git branch -d branchname```


### Pull

A `pull` in git is basically saying `get me all the new changes` that have been made in this repository.
When making a `pull` in git, we choose to specialize the `branch` we want to pull from. If no branch is specified, git automatically assumes you want to pull from the existing `branch`

This is done by executing the command

```$ git pull origin master``` 

`origin master` above is bascially saying get me all the changes that have been made in the master branch.
If we had another `branch` called `staging` and we wanted to pull from there, the command would have been like this :

```$ git pull origin staging```

### Add

When we make new changes in our git repository, we need to `add` them, and what this really means is to let git know that it should add it what is going to be committed.

This is done by executing the command

```$ git add filename```

Sometimes, it may be a little cubersome doing that for all the files we want to add. What we can do in this case is to run the command:

```$ git add . ```

And yeah, you guessed right. The command above adds all the changed files to what would committed.

### Commit

A `commit` in git is basically saying `store these recent changes` that have been made in my repository. 
This is done by executing the command

```$ git commit -m "message" ```

Every commit is usually accompanied by a message. This message is to allow someone else who takes a look at your repository understand exactly what you did and why you did what you did.

### Push

After we have made `commits` in our repostory, we need to push the changes to our remote repository on git. If we don't push the changes, the changes that have been made would only be known to our local computer. 

This is done by executing the command

```$ git push origin master``` 

`origin master` above is bascially saying `push all the changes` into the master branch.
If we had another `branch` called `staging` and we wanted to push to that branch, the command would have been like this :

```$ git push origin staging```

### Merge

Remember when we talked about branching yeah? When we are done implementing the changes in our branch and we are sure it works, we can decide to merge the changes to another branch. What is means is that we are `basically copying the new files into another branch`

This is done by executing the command:

```$ git merge branchname```

Keep in mind, when we are merging, we are saying 'take those changes and bring them here' so this means that , the merge command has to be executed in the branch we want to update.


Yeah, so those are some basics to get you up and running with git.
Happy #hacktoberfest 👩🏾‍💻 👨🏾‍💻 🔥