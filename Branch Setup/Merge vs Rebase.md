# Merging vs. rebasing
====================

The `git rebase` command has a reputation for being magical Git hocus pocus that beginners should stay away from, but it can actually make life much easier for a development team when used with care. In this article, we'll compare `git rebase` with the related `git merge` command and identify all of the potential opportunities to incorporate rebasing into the typical Git workflow.

* * * * *

## Conceptual overview
-------------------

* * * * *

The first thing to understand about `git rebase` is that it solves the same problem as `git merge`. Both of these commands are designed to integrate changes from one branch into another branch---they just do it in very different ways.

Consider what happens when you start working on a new feature in a dedicated branch, then another team member updates the `main` branch with new commits. This results in a forked history, which should be familiar to anyone who has used Git as a collaboration tool.

![A forked commit history](https://wac-cdn.atlassian.com/dam/jcr:1523084b-d05a-4f5a-bd1a-01866ec09ca3/01%20A%20forked%20commit%20history.svg?cdnVersion=1746)

Now, let's say that the new commits in `main` are relevant to the feature that you're working on. To incorporate the new commits into your `feature` branch, you have two options: merging or rebasing.

### The merge option

The easiest option is to merge the `main` branch into the feature branch using something like the following:

```
git checkout feature
git merge main
```

Or, you can condense this to a one-liner:

```
git merge feature main
```

This creates a new "merge commit" in the `feature` branch that ties together the histories of both branches, giving you a branch structure that looks like this:

![Merging main into feature branch](https://wac-cdn.atlassian.com/dam/jcr:4639eeb8-e417-434a-a3f8-a972277fc66a/02%20Merging%20main%20into%20the%20feature%20branh.svg?cdnVersion=1746)

Merging is nice because it's a *non-destructive* operation. The existing branches are not changed in any way. This avoids all of the potential pitfalls of rebasing (discussed below).

On the other hand, this also means that the `feature` branch will have an extraneous merge commit every time you need to incorporate upstream changes. If `main` is very active, this can pollute your feature branch's history quite a bit. While it's possible to mitigate this issue with advanced `git log` options, it can make it hard for other developers to understand the history of the project.

### The rebase option

As an alternative to merging, you can rebase the `feature` branch onto `main` branch using the following commands:

```
git checkout feature
git rebase main
```

This moves the entire `feature` branch to begin on the tip of the `main` branch, effectively incorporating all of the new commits in `main`. But, instead of using a merge commit, rebasing *re-writes* the project history by creating brand new commits for each commit in the original branch.

![Rebasing feature branch into main](https://wac-cdn.atlassian.com/dam/jcr:3bafddf5-fd55-4320-9310-3d28f4fca3af/03%20Rebasing%20the%20feature%20branch%20into%20main.svg?cdnVersion=1746)

The major benefit of rebasing is that you get a much cleaner project history. First, it eliminates the unnecessary merge commits required by `git merge`. Second, as you can see in the above diagram, rebasing also results in a perfectly linear project history---you can follow the tip of `feature` all the way to the beginning of the project without any forks. This makes it easier to navigate your project with commands like `git log`, `git bisect`, and `gitk`.