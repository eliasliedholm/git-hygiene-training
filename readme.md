# Git hygiene training

This repository is an interactive exercise that will help you master the git tools necessary to keep a clean history of your project. The exercise will cover the following topics:
- Rebase
- Force push
- Fixup
- Squash

This exercise requires a basic understanding of git command line tools for merging branches and commiting code. When you are ready to begin, simply follow the instructions below and learn by doing.

## Setup

  1. Fork this repository
  2. Clone the project to your desktop
  3. ▶️ Run `git merge introduction` to continue this exercise

## Summary

▶️ As a final repetition, don't forget to rebase with master to include all the previous sections. This time however you'll notice something that hasn't happened before. Because this branch have two commits, you will need to apply them both on the new base. This is different to when you are merging master into your branch, as it would apply all the new changes at once. When running `git rebase master` it will begin with letting you resolve the conflicts with your first commit from this branch, and then the second one, rather than both at once. Simply follow the instructions in the terminal.

### Hygiene
By planning our work, and learning how to clean up after pushing commits that lack structure, we can keep our git histories clean.

### Rebasing
Instead of merging master to get the latest changes added on top of yours, use rebasing to place your commits on top of the latest version of master.

### Force pushing
After changing the history on a branch, your changes can no longer be merged with the older version that is still on github. Use `git push --force` to override what is there with the exact state of your local branch.

### Fixups
Fixups allows you to correct mistakes in previous commits.

### Interactive Rebasing
Interactive rebasing provides a set of options to edit the history.
  - **squash** together multiple commits into a single one.
  - **reword** commit messages
  - **edit** the code inside a commit
  - **drop** a commit entirely