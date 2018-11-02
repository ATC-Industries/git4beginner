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
