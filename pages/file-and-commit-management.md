# Commands for managing files and commits

## `git mv`

This command moves or renames files. It is a combination of `git rm` and `git add`.

## Useful forms

<dl>
  <dt><code>git mv &lt;filepath&gt; &lt;new filepath&gt;</code></dt>
  <dd>Move a file while keeping track of it in Git.</dd>
</dl>

## Assignment 10

Rename the `new-file.md` file to `old-file.md` and commit the change.

## `git rm`

This command deletes files and stops git from tracking the file.

## Useful forms

<dl>
  <dt><code>git rm &lt;filepath&gt;</code></dt>
  <dd>Delete a specific file and remove it from tracking</dd>
</dl>

## Assignment 12

Delete `old-file.md` and commit the change.

## `git revert`

This command creates a new commit that reverses changes in a specific commit in the branch history.

## Useful forms

<dl>
  <dt><code>git revert &lt;commit hash&gt;</code></dt>
  <dd>Undo the changes done in a commit in a new commit.</dd>
</dl>

<details>
  <summary>Assignment 12</summary>
  <p>Undo the deletion and renaming of the <code>new-file.md</code> file.</p>
</details>

## `git cherry-pick`

This command lets you replay commit changes from one branch into your current branch.

## Useful forms

<dl>
  <dt><code>git cherry-pick &lt;commit hash&gt;</code></dt>
  <dd>Apply a single commit change.</dd>
</dl>

<dl>
  <dt><code>git cherry-pick &lt;commit hash1&gt; &lt;commit hash2&gt; ...</code></dt>
  <dd>Apply multiple commit changes in the given order.</dd>
</dl>

<details>
  <summary>Assignment 13</summary>
  <ul>
    <li>Create a new branch called <code>combined</code> off the <code>master</code> branch.</li>
    <li>Use <code>git log</code> to identify your changes in the <code>add-new-file</code> and <code>sequence</code> branches.</li>
    <li>Cherry pick the unique changes from the <code>add-new-file</code> and <code>sequence</code> branches into this one.</li>
  </ul>
</details>

<br/>

**[Next lesson: Dangerous commands](dangerous-commands.md)**
