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
