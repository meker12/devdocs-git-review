# Basic workflow commands

## `git branch`

This command lets you manage your branches.

### Useful forms

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

<details>
  <summary>Assignment 3</summary>
  <ul>
    <li>Create a local branch</li>
    <li>Verify that the branch has been created by listing your local branches</li>
    <li>Delete the branch you just created</li>
    <li>List your local branches and verify the branch has been deleted</li>
  </ul>
</details>

## `git checkout`

This command lets you navigate through the different branches in your repo.

### Useful forms

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

<details>
  <summary>Assignment 4</summary>
  <p>
    Create and switch to a new local branch that is based off the remote branch named <code>sequence</code>.
    Verify you are in the correct branch and that it is linked to a remote branch by using <code>git status</code>.
  </p>
</details>

## `git add`

This command stages modified files for commit or adds untracked files to the next commit.

### Useful forms

<dl>
  <dt><code>git add .</code></dt>
  <dd>Adds all unstaged changes to the next commit.</dd>
</dl>

<dl>
  <dt><code>git add &lt;filepath1&gt; &lt;filepath2&gt; ...</code></dt>
  <dd>Adds specific files to the next commit.</dd>
</dl>

<details>
  <summary>Assignment 5</summary>
  <ul>
    <li>Modify the <code>sequence.md</code> file and add a new list item.</li>
    <li>Create a new file called <code>new-file.md</code> and add some random content.</li>
    <li>Stage <strong>only</strong> the <code>sequence.md</code> file for commit.</li>
  </ul>
</details>

## `git commit`

Adds all staged changes to a new commit with a commit message summary and optional description.

A good commit message summary should be limited to 50 characters and complete the following sentence:

>When this commit is applied it will...

Additional information about the change should go into the commit description.

For more guidance, see: [How to Write a Git commit message](https://chris.beams.io/posts/git-commit/)

### Useful forms

<dl>
  <dt><code>git commit -m "&lt;commit message&gt;"</code></dt>
  <dd>Creates a new commit with the specific commit message</dd>
</dl>

<dl>
  <dt><code>git commit</code></dt>
  <dd>Opens an editor that lets you write a multi-line commit message before creating the new commit.</dd>
</dl>

<details>
  <summary>Assignment 6</summary>
  <p>Create a new commit with your staged changes and a meaningful commit message.</p>
</details>

<br/>

**[Next lesson: Commands for working with remote repositories](working-with-remote-repos.md)**
