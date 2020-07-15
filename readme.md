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

## Introduction to git hygiene

A clean git history means that your commits are neatly organised chronologically and are including information that is relevant and helpful to the people collaborating on a project.

A common way for teams to use git is by branching out when developing a feature and continuously merge the master branch back into their feature branch. This causes the history to list commits not based on when they were
merged to master, but when they were written in the first place, resulting in a history that looks something like this:

```
[banana] add tests for banana feature
Merge branch 'apple' into master
[apple] added tests for apple feature
[banana] use the refactored components in my new feature
Merge branch 'orange' into master
[orange] Merge branch 'master' into orange
[orange] added orange feature
[apple] Merge branch 'master' into apple
[banana] refactored existing components before using them in banana feature
```

While this history is true in the sense that presents everything that has happened, there are a couple of things that are hard to do. Consider this:
  - Can you easily see which commits that belong to the branch `banana`? What if the feature was developed over a couple of weeks and the history have over hundreds of commits just in the last week?
  - Is all the information relevant? Do I care about the fact that `master` was merged into `orange`, which in turn was merged back into `master`?
  - What if there is a bug in the branch `orange` and I want to revert it? Can I simply revert the merge commit? What if `orange` already contains commits from `apple` after `master` was merged into it?

▶️ Let's learn how we can do better! Run `git checkout rebasing` to continue.