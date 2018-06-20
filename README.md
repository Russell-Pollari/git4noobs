# Git4n00bs

A swift intro to Git and GitHub for noobs. Contributions welcome!

## Getting started

1. [install Git](https://git-scm.com/book/en/v1/Getting-Started-Installing-Git).  
1. Make a GitHub account.
1. Open a terminal!
Git is best utilized [on the command line](https://git-scm.com/book/en/v2/Getting-Started-The-Command-Line).

## Pre-reqs
When this spits out a version number:
```
$ git --version
```
and you have an account on GitHub, we're good to go.

## Configure git
```
$ git config --global user.name <your_name>
$ git config --global user.email <your_email>
```
The global tag means these will be used by default in all of your local respositories. When you are in a git repository, there will be a local config which can be accessed by replacing `--global` with `--local`.

To list all your global git config values
```
$ git config --global -l
```

Git makes it easy to collaborate on software projects, like this one!

## Fork this repository
In the top-right corner of the page, click **Fork**.

This creates a copy of this repository on your GitHub account.

## Clone your forked repository
We need to make a local copy of this repository on your computer.
```
$ git clone <repo_URL>
```
**n00b tip**: `repo_URL` can be found from the <kbd>Clone or download</kbd> button on the top right of the GitHub page.

Navigate to the newly created directory.
```
$ cd git4noobs
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
```

You will see the github url for the repo in the local config values as `remote.origin`
```
$ git config --local -l

```

## Make a new branch
When you want to start making changes, you make a branch. This will leave the code in the `master` branch (conventional name for the main/production-ready branch) and all your changes will be isolated to your newly created branch.

To list your repository's branches:
```
$ git branch
* master
```

Create a new branch:
```
$ git branch my-branch
```
and then go to it
```
$ git checkout my-branch
```

The two lines above can be shortcutted with:
```
$ git checkout -b my-branch
```

You should now see your newly created branch in the list.
```
$ git branch
  master
* my-branch
```

## Edit this README
Time to make some changes to commit.  

Open README.md in your favourite editor.

Every repository should have a README file. It's what's displayed on the repo's GitHub page. This README is a [markdown file](https://learn.getgrav.org/content/markdown), which has an easy to use syntax for making your README look good.

Add your gitHub username to the Contribuots list at the end of this document and save.
(or really, make any edit you want to)

## Make a commit
Now you have unsaved changes in your working directory. To see a summary:
```
$ git status
On branch my-branch
Your branch is up-to-date with 'origin/my-local-branch'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```
You can look at the changes you've made
```
$ git diff
```
**n00b tip:** use <kbd>enter</kbd> to scroll and <kbd>q</kbd> to exit)

Stage your changes for commit (aka yes I want to keep these changes)
```
$ git add README.md
```
You can discard changes from your woeking directory
```
$ git checkout README.md
```
Your changes are now staged for commit.
```
$ git status
On branch my-local-branch
Your branch is up-to-date with 'origin/my-local-branch'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	modified:   README.md
```
When changes are staged, they are ready to be added to the codebase, we just
need to give the change a name. That is what a commit is.

Now, commit with a clear, concise message:
```
$ git commit -m "Add name to contributors"
```
(adjust the message accordingly if you added/changed anythings else )
<!-- TODO: git messages in editor and git config to set default editor -->

See [this blog post](https://chris.beams.io/posts/git-commit/) for good practices with commit messages.

You can take a look at the commit history using:
```
$ git log
```  
**n00b tip:** use <kbd>enter</kbd> to scroll and <kbd>q</kbd> to exit)  

Most `git` commands have alot of options. For example, for a prettier view of the commit/branch history:
```
$ git  log --oneline --graph
```
Use `-h` to get help on any git command (e.g. `$ git -h` or `$ git commit -h`)

## Push your changes to remote

The changes you've made are only on your local repository. Push your branch to the remote repository:
```
git push origin my--branch
```
Your branch is now on your remote repository.

**n00b tip:** `origin` is an alias for the remote repository which was automatically created when you cloned the repo.

## Create a pull request
You've almost contributed to this tutorial!
The last step is to merge your branch into the master branch of the original repository.

Since you are not an owner of the original repo, you will have to create a pull-request.
This is a request to add your changes to the code, which the owner can approve.

On the GitHub page for your page, find the <kbd>New pull request</kbd> button, and create a pull request merging your branch (head fork) into the master of the original repo (base fork).

## Conclusion

Congrats you have succesfully contributed to a public git repo!
We've only glimpsed at what git can do, especially with GitHub. But now you have used
it and the ice is broken.
To learn more advanced Git commands, the [Git docs](https://git-scm.com/docs) are
a good place to start.

If you feel like something was missing, or poorly explained, feel free to create a new pull-request with your changes.

## Contributors
- Russell Pollari
- Joe Test
- Ben Geraedts
