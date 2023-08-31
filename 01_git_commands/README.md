# Git & Github

[Git commands](#git-commands)

- [Getting & Creating](#getting-and-creating)
- [Basic Snap-shooting](#basic-snapshotting)
- [Sharing and Updating Projects](#sharing-and-updating-projects)
- [Remove and change remote](#remove-and-change-the-url-for-a-remote-git-repository)
- [Inspection and Comparison](#inspection-and-comparison)
- [Branching](#branching-commands)

<br/>

5. [Push your code to Github](#push-your-code-to-github)
6. [Pull changes from remote repo](#pull-changes-from-remote-repo-to-your-local-machine)
7. [Git Branching](#git-branching)
8. [External Resources](#external-resources)

<br/>

# Terms:

| Term                   | Short definition                                                                                     |
| ---------------------- | ---------------------------------------------------------------------------------------------------- |
| Git                    | Free and open source version control system                                                          |
| Version control system | The management of changes on our code                                                                |
| Repository             | The place where your project is kept                                                                 |
| Repo                   | Short for Repository                                                                                 |
| Local Repo             | Where your project is locally kept                                                                   |
| Remote Repo            | Where your project is remotely kept                                                                  |
| Github                 | A website to host your repositories online                                                           |
| Branch                 | Where an updated copy of the main code is kept without affecting the main version with those changes |

<br/>

# The benefits of Version Control:

- Save an initial version of our code
- Register a complete long-term change history of every file
- Branching -> keeps multiple copies of work independent from each other
- Merging -> providing the facility to merge that work back together
- Being able to trace each change made to the project

<br/>

# Git commands

## Getting and Creating

| Command                                                    | Description                                |
| ---------------------------------------------------------- | ------------------------------------------ |
| `git init`                                                 | Initialize a local Git repository          |
| `git clone git@github.com[username]/[repository-name].git` | Create a local copy of a remote repository |

<br/>

## Basic Snapshotting

| Command                          | Description                                        |
| -------------------------------- | -------------------------------------------------- |
| `git status`                     | Check the status of the repository and its content |
| `git add [file-name]`            | Add the specified file to the staging area         |
| `git add .`                      | Add all new and changed files to the staging area  |
| `git commit -m "commit message"` | Save your changes in Git                           |
| `git rm -r [file/dir-name]`      | Remove a file (or directory)                       |

<br/>

## Sharing and Updating Projects

| Command                                                                | Description                                                       |
| ---------------------------------------------------------------------- | ----------------------------------------------------------------- |
| `git push origin [branch name]`                                        | Push changes to your remote repository                            |
| `git push -u origin [branch name]`                                     | Push changes to remote repository (and ste the branch as default) |
| `git push`                                                             | Push changes to remote repository (default branch)                |
| `git push origin --delete [branch name]`                               | Delete a remote branch                                            |
| `git pull origin [branch name]`                                        | Pull changes from remote repository                               |
| `git remote add origin git@github.com[username]/[repository-name].git` | Add a remote repository                                           |

<br/>

## Remove and change the URL for a remote git repository

| Command                                   | Description                                                                   |
| ----------------------------------------- | ----------------------------------------------------------------------------- |
| `git remote -v`                           | View all the remotes of our local repository                                  |
| `git remote rm [name of the remote)]`     | Remove a remote connection.                                                   |
| `git remote set-url origin [new git url]` | Create new remote connection called origin (you can also choose another name) |

In the following example the remote is called `origin`

```
zkh@zkh ~/Desktop/square (main) $ git remote -v
>> origin	git@github.com:ZakariaHn/square.git (fetch)
>> origin	git@github.com:ZakariaHn/square.git (push)

```

<br/>

## Inspection and Comparison

| Command                                   | Description                    |
| ----------------------------------------- | ------------------------------ |
| `git log`                                 | View changes                   |
| `git log --summary`                       | View changes (detailed)        |
| `git log --oneline`                       | View changes (briefly)         |
| `git diff [source branch] [target branch` | Preview changes before merging |

<br/>

# Branching

In a nutshell, Git branches allow developers to diverge from the main branch by creating separate branches to isolate code changes. The default branch in Git is the master branch and any other branch we create is referred to as a feature branch and we have the permission to name it whatever we want.

<br/>

> If you initialize you repository locally, the default branch will be called master.
> GitHub replaced the term "master" on its service with a neutral term like "main" to avoid any negative associations with the term "master".

<br/>

### Branching Commands

| Command                                             | Description                                             |
| --------------------------------------------------- | ------------------------------------------------------- |
| `git branch`                                        | List branches (the asterisk denotes the current branch) |
| `git branch -a`                                     | List all branches (local and remote)                    |
| `git branch [branch name]`                          | Create a new branch                                     |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch                                   |
| `git branch -d [branch name]`                       | Delete a branch                                         |
| `git push origin --delete [branch name]`            | Delete a remote branch                                  |
| `git clone -b [branch name] [remote repo-url]`      | Clone a remote branch                                   |
| `git checkout [branch name]`                        | Switch to another branch                                |
| `git checkout -b [branch name]`                     | Create a new branch and switch to it                    |
| `git checkout -`                                    | Switch to the branch last checked out                   |
| `git checkout -- [file-name.txt]`                   | Discard changes to a file                               |
| `git switch -c [new branch name]`                   | Create a new branch                                     |
| `git switch [existing branch name]`                 | Switch to another branch                                |

<br/>

> The "switch" command is relatively new (added in Git v2.23) and provides a simple alternative to the classic "checkout" command..
>
> It has a very clear and limited purpose: switching and creating branches!

<br/>

<br/>

## External Resources

---

- [Learn Git Branching visually](https://www.atlassian.com/git/tutorials/saving-changes)
- [Git and Github Visualized (video about the game in the link above)](https://www.youtube.com/watch?v=p384Hw2eewA)
- [What is Git?](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F#what_is_git_section)
- [Saving changes](https://www.atlassian.com/git/tutorials/saving-changes)
- [Git Behind the Scenes: How Does Git Work (video)](https://www.youtube.com/watch?v=gzJk1ruqSok)
- [Deleting your git commit history without removing repo on Github](https://www.willandskill.se/en/deleting-your-git-commit-history-without-removing-repo-on-github-bitbucket/)
