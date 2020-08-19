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

## Interactive rebasing

A key factors to being successful with git hygiene is dicipline. But things don't always go as we planned, a lot can happen during the development of a feature that might make it hard to keep commits clean. You might find yourself with a branch full of commits with bad hygiene. In that situation, interactive rebasing provides us with a set of options to help us restore a clean log. In the previous step you already learned how to do a fixup, now lets look at how we can squash some commits together.

▶️ Run `git log --oneline` to see the commits on this branch that we want to squash.

▶️ Run `git rebase master -i` to start an interactive rebase, which will open an editor where we can specify the commits we want to squash.

▶️ In order to squash the last three commits with the first one, replace the word `pick` with `squash`. This would also be a good time to change the message of the first commit, in order to do so we instead replace `pick` with `reword`.
  ```
  reword e3439fa Add instructions on how to squash commits
  squash d010d43 Begin writig instructions
  squash 3fdcac2 Here have some more instructions
  ```

▶️ After saving and closing the editor, the next step will begin immediately and a new editor will appear. This time you will have the chance to reword the first commit. Let's change it to `Add instructions on how to squash commits`, then save and close. After this, all changes of the following commits will automatically be made part of the first commit.

▶️ Run `git log --oneline` again to verify that the history in fact looks clean now. If it is, let's checkout master and merge this branch.

### More options
You just learned how to squash together and reword commits, interactive rebasing offer a few more tools that wont be covered here, such as `edit` and `drop` which allows you to edit code, or drop a commit from the history completely.

▶️ For a final summary, checkout the branch `summary`.