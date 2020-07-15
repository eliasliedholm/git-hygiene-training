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

## Fixups

▶️ Before we begin, remember to rebase since the base of this branch is now behind master. Run `git rebase master` to make sure this branch includes the introduction and rebasing sections.

We all make mistakes, and thats fine, but if our ambitions is to keep a clean log, we need a way to Correct our misstakes. The sentence you just read include a couple of grammatical errors. The problem is that they have already been committed. We could simply correct the mistakes and commit the changes, but that would leave an obvious trail that all of your collaborators would be able to track down for all eternity. Embarrasing.

Beyond just being embarrasing, it can be quite hard to get an idea of what changes are included on your branch when half of the commits are "fix spelling mistake" or "work in progress". That's when a fiuxp comes in handy!

▶️ Run `git log --oneline` and copy the hash of the commit from the fixup branch, it shuold be the one on the very top.

▶️ Correct the mistakes in the sentence above and stage your changes with `git add readme.md`

▶️ Commit your changes as a fixup to the original commit by `git commit --fixup {{hash}}`, remember to replace {{hash}} with the hash you copied from the log.

▶️ Fianlly, pretend like noting ever happened by rebasing with the autosquash command: `git rebase -i --autosquash master`, don't forget to force push as well so no one will ever know.

▶️ Merge this section into master and check out the next step where we will learn how to further edit our history with the interactive rebase. Use `git checkout interactive` to continue.