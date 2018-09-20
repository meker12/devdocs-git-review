# Commands for working with remote repositories

## `git fetch`

This command updates your local commit references with changes in a remote repository.

### Useful forms

<dl>
  <dt><code>git fetch &lt;remote name&gt;</code></dt>
  <dd>Updates the local commit references with the named remote.</dd>
</dl>

<dl>
  <dt><code>git fetch &lt;remote name&gt; -p</code></dt>
  <dd>Updates the local commit references and prunes/deletes remote branch references.</dd>
</dl>

<details>
  <summary>Assignment 7</summary>
  <p>Get the most recent changes from this repository.</p>
</details>

## `git merge`

This command merges commits to the current branch and creates a unified history.

### Useful forms

<dl>
  <dt><code>git merge &lt;branch name&gt;</code></dt>
  <dd>Merge the changes from another branch into this one and create a new merge commit.</dd>
</dl>

<dl>
  <dt><code>git merge &lt;remote name&gt;/&lt;branch name&gt;</code></dt>
  <dd>Merge the changes from a remote branch into this one and create a new merge commit.</dd>
</dl>

<dl>
  <dt><code>git merge --ff-only &lt;branch name&gt;</code></dt>
  <dd>Moves the commit pointer to the most recent commit of the incoming branch. Only works if there have been no changes to the current branch.</dd>
</dl>

<dl>
  <dt><code>git merge --continue</code></dt>
  <dd>Continues the merging process after resolving merge conflicts.</dd>
</dl>

<dl>
  <dt><code>git merge --abort</code></dt>
  <dd>Aborts the merge process when a merge conflict occurs.</dd>
</dl>

<details>
  <summary>Assignment 8</summary> 
  <p>Merge the new <code>sequence-edit</code> branch from this repository into your current branch and resolve the merge conflicts.</p>
</details>

## `git pull`

This command combines `git fetch` and `git merge` into a single command.

### Useful forms

<dl>
  <dt><code>git pull &lt;remote name&gt;</code></dt>
  <dd>Fetch the remote copy of the current branch and do a merge.</dd>
</dl>

## `git push`

This command updates a remote repository branch.

### Useful forms

<dl>
  <dt><code>git push &lt;remote name&gt; &lt;branch name&gt;</code></dt>
  <dd>Pushes your branch changes to the specified remote repository branch. A new branch is created if it does not already exist.</dd>
</dl>

<dl>
  <dt><code>git push -u &lt;remote name&gt; &lt;branch name&gt;</code></dt>
  <dd>Same as the previous command but also links this branch to the remote repository branch.</dd>
</dl>

<details>
  <summary>Assignment 9</summary> 
  <ul>
    <li>Create a new branch called <code>add-new-file</code> off the <code>master</code> branch.</li>
    <li>Add the untracked <code>new-file.md</code> file to the stage and commit.</li>
    <li>Push this new branch to your remote repository and link the remote branch to your local branch.</li>
  </ul>
</details>

<br/>

**[Next lesson: File and commit management commands](file-and-commit-management.md)**
