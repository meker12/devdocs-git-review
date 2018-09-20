# Git commands review for DevDocs

This repo is a sandbox for learning the git commands used in everyday DevDocs tasks.

In order to use this repository, start by forking the repository in GitHub.

<dl>
  <dt>Git fork:</dt>
  <dd>A Git fork is a server side clone on a Git repository. It is not a regular git command but rather a type of software development approach.</dd>
</dl>

## Basic commands

### `git clone`

This command copies a remote repository into your local machine.

### Useful forms

<dl>
  <dt><code>git clone &lt;URL&gt;</code></dt>
  <dd>Copies the repository at the URL into a local directory</dd>
</dl>

#### Assignment 1

Create a local clone of the your forked repo and navigate to it.

### `git status`

This command provides useful information about the state of your repository.

### `git log`

Shows you a list of commit messages for the current branch.

### `git remote`

This command helps you manage your remote repositories.

### Useful forms

<dl>
  <dt><code>git remote -v</code></dt> 
  <dd>Shows a list of remote repositories.</dd>
</dl>

<dl>
  <dt><code>git remote add &lt;name&gt; &lt;URL&gt;</code></dt>
  <dd>Adds a remote repository at the specified URL. This repository can be referenced using the name provided.</dd>
</dl>

<dl>
  <dt><code>git remote rm &lt;name&gt;</code></dt>
  <dd>Deletes the remote repository identified using the given name.</dd>
</dl>

#### Assignment 2

Add the original repository as a remote and verify by listing your remote repositories.

### `git branch`

This command lets you manage your branches.

#### Useful forms

<dl>
  <dt><code>git branch</code></dt>
  <dd>Lists all your local branches.</dd>
</dl>

<dl>
  <dt><code>git branch -a</code></dt>
  <dd>Lists local and remote branches.</dd>
</dl>

<dl>
  <dt><code>git branch &lt;branch name&gt;</code></dt>
  <dd>Create a new branch off the most recent commit.</dd>
</dl>

<dl>
  <dt><code>git branch -d &lt;branch name&gt;</code></dt>
  <dd>Deletes a local branch.</dd>
</dl>

#### Assignment 3

* Create a local branch
* Verify that the branch has been created by listing your local branches
* Delete the branch you just created
* List your local branches and verify the branch has been deleted

### `git checkout`

This command lets you navigate through the different branches in your repo.

#### Useful forms

<dl>
  <dt><code>git checkout &lt;branch name&gt;</code></dt>
  <dd>Switches to the specific branch name.</dd>
</dl>

<dl>
  <dt><code>git checkout -b &lt;branch name&gt;</code></dt>
  <dd>Create a new branch with the specific name and switch to it.</dd>
</dl>

<dl>
  <dt><code>git checkout -b &lt;branch name&gt; &lt;remote name&gt;/&lt;remote branch name&gt;</code></dt>
  <dd>Create a new branch based on a remote branch and set the upstream of the new branch to the remote branch.</dd>
</dl>

<dl>
  <dt><code>git checkout &lt;remote name&gt;/&lt;branch name&gt;</code></dt>
  <dd>Switch to the commit pointed to by a remote branch. This will put you in headless mode.</dd>
</dl>

<dl>
  <dt><code>git checkout &lt;commit hash&gt;</code></dt>
  <dd>Switch to a specific commit hash. This will put you in headless mode.</dd>
</dl>

<dl>
  <dt><code>git checkout &lt;filepath&gt;</code></dt>
  <dd>Undo all changes done to an unstaged file and revert the content to the most recent commit.</dd>
</dl>

#### Assignment 4

Create and switch to a new local branch that is based off the remote branch named `sequence`.
Verify you are in the correct branch and that is is linked to a remote branch by using `git status`.

Your output should contain a section that looks like the following:

```sh
On branch sequence
Your branch is up to date with 'jcalcaben/sequence'.
```

### `git add`

This command stages modified files for commit or adds untracked files to the next commit.

#### Useful forms

<dl>
  <dt><code>git add .</code></dt>
  <dd>Adds all unstaged changes to the next commit.</dd>
</dl>

<dl>
  <dt><code>git add &lt;filepath1&gt; &lt;filepath2&gt; ...</code></dt>
  <dd>Adds specific files to the next commit.</dd>
</dl>

#### Assignment 5

* Modify the `sequence.md` file and add a new list item.
* Create a new file called `new-file.md` and add some random content.
* Stage **only** the `sequence.md` file for commit.

### `git commit`

Adds all staged changes to a new commit with a commit message summary and optional description.

A good commit message summary should be limited to 50 characters and complete the following sentence:

>When this commit is applied it will...

Additional information about the change should go into the commit description.

For more guidance, see: [How to Write a Git commit message](https://chris.beams.io/posts/git-commit/)

#### Useful forms

<dl>
  <dt><code>git commit -m "&lt;commit message&gt;"</code></dt>
  <dd>Creates a new commit with the specific commit message</dd>
</dl>

<dl>
  <dt><code>git commit</code></dt>
  <dd>Opens an editor that lets you write a multi-line commit message before creating the new commit.</dd>
</dl>

#### Assignment 6

Create a new commit with your staged changes and a descriptive commit message.

## Advanced commands

### `git fetch`

This command updates your local commit references with changes in a remote repository.

#### Useful forms

<dl>
  <dt><code>git fetch &lt;remote name&gt;</code></dt>
  <dd>Updates the local commit references with the named remote.</dd>
</dl>

<dl>
  <dt><code>git fetch &lt;remote name&gt; -p</code></dt>
  <dd>Updates the local commit references and prunes/deletes remote branch references.</dd>
</dl>

#### Assignment 7

Get the most recent changes from this repository.

### `git merge`

This command merges commits to the current branch and creates a unified history.

#### Useful forms

`git merge <branch name>`
Merge the changes from another branch into this one and create a new merge commit.

`git merge <remote name>/<branch name>`
Merge the changes from a remote branch into this one and create a new merge commit.

`git merge --ff-only <branch name>`
Moves the commit pointer to the most recent commit of the incoming branch. Only works if there have been no changes to the current branch.

`git merge --continue`
Continues the merging process after resolving merge conflicts.

`git merge --abort`
Aborts the merge process when a merge conflict occurs.

#### Assignment 8

Merge the new `sequence-edit` branch from this repository into your current branch and resolve the merge conflicts.

### `git pull`

This command combines `git fetch` and `git merge` into a single command.

#### Useful forms

`git pull <remote name>`
Fetch the remote copy of the current branch and do a merge.

### `git push`

This command updates a remote repository branch.

#### Useful forms

`git push <remote name> <branch name>`
Pushes your branch changes to the specified remote repository branch. A new branch is created if it does not already exist.

`git push -u <remote name> <branch name>`
Same as the previous command but also links this branch to the remote repository branch.

#### Assignment 9

* Create a new branch called `add-new-file` off the `master` branch.
* Add the untracked `new-file.md` file to the stage and commit.
* Push this new branch to your remote repository and link the remote branch to your local branch.

### `git cherry-pick`

This command lets you replay commit changes from one branch into your current branch.

#### Useful forms

`git cherry-pick <commit hash>`
Apply a single commit change.

`git cherry-pick <commit hash1> <commit hash2> ...`
Apply multiple commit changes in the given order.

#### Assignment 10

* Create a new branch called `combined` off the `master` branch.
* Use `git log` to identify your changes in the `add-new-file` and `sequence` branches.
* Cherry pick **only** your changes from the `add-new-file` and `sequence` branches into this one.

### `git mv`

This command moves or renames files. It is a combination of `git rm` and `git add`.

#### Useful forms

`git mv <filepath> <new filepath>`
Move a file while keeping track of it in Git.

#### Assignment 11

Rename the `new-file.md` file to `old-file.md` and commit the change.

### `git rm`

This command deletes files and stops git from tracking the file.

### Useful forms

`git rm <filepath>`
Delete a specific file and remove it from tracking

#### Assignment 12

Delete `old-file.md` and commit the change.

### `git revert`

This command creates a new commit that reverses changes in a specific commit in the branch history.

#### Useful forms

`git revert <commit hash>`
Undo the changes done in a commit in a new commit.

#### Assignment 12

Undo the deletion and renaming of the `new-file.md` file.

## Dangerous commands

### `git commit --amend`

### `git push -f`

### `git reset`

### `git rebase`
