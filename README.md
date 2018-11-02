# git4beginner
A practice repo with some beginner info


## Pulling

When you start programming you will want to PULL the most recent code base from the cloud.

1. Go to the folder in cmd prompt

`cd ~users/projects/workingFolder` for example

Once in the folder you will want to pull any changes that may have been made so you are working on the most recent codebase.

`git pull`

Now you can start working on your code.  Don't forget to commit often.

## Committing

Once you’ve made a change to a file you will want to commit it.

_Commit Early And Often_

The process of making a commit is as follows:
1. add files to the staging area.
2. write a commit message.
3. commit files to your local git repo. (later we will push all your commits to gitHub)

First you need to add the files you want to commit to the “staging area”

`git add [filename]`
OR
`git add .`
(The period means add all files that have changed since the last commit, I use this one the most)

Once you've added files to the staging area you can look at them to see they are there.  
`git status`
This is good practice

Finally we can commit the changes:

`git commit -m “TYPE: subject”`

### The Type

The type is contained within the title and can be one of these types:
* feat: a new feature
* fix: a bug fix
* docs: changes to documentation
* style: formatting, missing semi colons, etc; no code change
* refactor: refactoring production code
* test: adding tests, refactoring test; no production code change
* chore: updating build tasks, package manager configs, etc; no production code change

### The Subject
Subjects should be no greater than 50 characters, should begin with a capital letter and do not end with a period.
Use an imperative tone to describe what a commit does, rather than what it did. For example, use change; not changed or changes.

## Push
Finally when you are ready to send all your changes to git hub you simply type:
`git push`

Okay now, if no one has messed with the master branch since the last time you pulled then you should be able to `push` without any problems.

If however someone else has already made changes to the master you will be prompted to do a `git pull` to align the files.
```
$ git push
To https://github.com/ATC-Industries/git4beginner.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/ATC-Industries/git4beginner.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.```

So now you will want to do a `git pull` and one of two things will happen.  If the changes to the master are in different lines then the changes you are trying to push, the system will auto merge.  however.  If the changes are on the same lines you will need to select A, B or neither and then `git add .` `git commit` and `git push` again.

To manage merge conflicts I recommend using a text editor like atom as it has built in tools to assist you.

## Branching

The other alternative to managing merge conflicts locally is to NOT work on the master branch and instead work on a special branch and then later merge that branch to the master using the built in tools on gitHub.

* ```$ git branch```
Lists all local branches in the current repository
* ```$ git branch [branch-name]```
Creates a new branch
* ```$ git checkout [branch-name]```
Switches to the specified branch and updates the working directory
* ```$ git merge [branch]```
Combines the specified branch’s history into the current branch
* ```$ git branch -d [branch-name]```
Deletes the specified branch

#### So create your Branch
`git branch adamsTestBranch`
#### Then "checkout" that branch
`git checkout adamsTestBranch`

Now you can make changes all you want to that and we can later merger that branch into the master on GitHub and use the Github merge conflict tools.

## Pull Request

Go to gitHub and do a pull request!

