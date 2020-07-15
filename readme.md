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

## Rebasing

We have just learned why simply merging master into our feature branch can cause trouble, so what's the alternative? – It comes down to unlearning the idea of "getting the latest changes from master" to instead replace with "applying my changes on the latest version of master". You effectively want to start from scratch, using the latest version of master as a new base.

In the previous step, you merged the introduction branch into master. Instead of merging master into this branch to get those changes, let's try to rebase.

▶️ Run `git rebase master`, this will begin the rebasing. Because both branches have changes in the same place, you need to resolve a conflict. Solve it by placeing the instruction section before this section. Then stage your changes using `git add readme.md` and continue with `git rebase --continue`.

▶️ Run `git log --oneline` to see that the commit of the rebasing branch are in fact listed _after_ the introduction commit (while remembering that the log shows latest commits on the top).

▶️ When you have confirmed that your log looks the way you expect, run `git status`. This will reveal that your local branch have diverged from origin/rebasing. This is because you have rewritten the history, and the commits on origin no longer exist on your local branch, instead you have created new commits that include your changes, added after the introduction which were the latest version of master that you have now set to be your new base.

▶️ Now you must **resist the temptation of doing what git tells you to do**. If you pull, you will create a history that includes the commits from this branch before it was rebased, as well as after. Meaning everything will be duplicated. Ouch. Instead you need to replace the commits on the origin using a force-push. Run `git push --force`.

▶️ Finally you can `git checkout master` and `git merge rebasing` to add this section to your master branch. After this continue the exercise with `git checkout fixups`.