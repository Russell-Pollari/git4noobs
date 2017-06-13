# Git4n00bs

A beginnner's introduction to Git and GitHub basics.

## Getting started

1. [install Git]( https://git-scm.com/book/en/v1/Getting-Started-Installing-Git
).  
1. Make a GitHub account.
1. Open a terminal!
Git is best utilized [on the command line](https://git-scm.com/book/en/v2/Getting-Started-The-Command-Line).

## Configure git
```
$ git config --global user.name="<your-name-here>"
$ git config --global user.email="<your-email-here>"
```
The global tag means these will be used by default in all of your local respositories. Each git repo also has a local config which can be accessed by replacing `--global` with `--local`.

To list all your git config values
```
$ git config --global -l
```
## Clone this repository
Make a local copy of this repository on your computer.

Navigate and/or create a directory to keep your local repository.
```
$ mkdir git-tutorials
$ cd git-tutorials
$ git clone https://github.com/Russell-Pollari/git4noobs.git
```
**n00b tip**: the clone url can be found from the <kbd>Clone or download</kbd> button on the top right of the GitHub page.

Navigate to the newly created directory.
```
$ cd git4noobs
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
```

## Make a new branch
List your repository's branches:
```
$ git branch
* master
```

Create a new branch:
```
$ git branch my-local-branch
$ git checkout my-local-branch
```
or:
```
$ git checkout -b my-local-branch
```
You should now see your newly created branch in the list.
```
$ git branch
  master
* my-local-branch
```

## Edit this README
Time to make some changes to commit.  

Open README.md in your favourite editor.

**n00b tip:** Every repository should have a README file. It's what's displayed on the repo's GitHub page. This README is a [markdown file](https://learn.getgrav.org/content/markdown), which has an easy to use syntax for making your README look good. If your using [atom](https://atom.io/) for editing, you can preview a markdown file with <kbd>Ctl</kbd> + <kbd>Shift</kbd> + <kbd>m</kbd>.

Add your name to the list at the end of this document and save.

## Make a commit
after you save your change
```
$ git status
On branch my-local-branch
Your branch is up-to-date with 'origin/my-local-branch'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```
stage your changes for commit
```
$ git add README.md
```
or, to stage all files:
```
$ git add .
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
Now commit with a clear, concise message.
```
$ git commit -m "Add name to contributors"
```
<!-- TODO: git messages in editor and git config to set default editor -->
See [this blog post](https://chris.beams.io/posts/git-commit/) for good practices with commit messages.

You can take a look at the commit history using:
```
$ git log
```  
(noob tip: use <kbd>enter</kbd> to scroll and <kbd>q</kbd> to exit)  


Most `git` commands have alot of options. For example, for a prettier view of the commit/branch history:
```
$ git  log --oneline --graph
```
## Push your changes to remote

The changes you've made are only on your local repository.
```
git push origin my-local-branch
```
`origin` is an alias for the remote repository which was automatically created for you when cloned the repo.

## Contributors
1. Russell Pollari
