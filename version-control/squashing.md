# Squashing

![image](https://github.com/beranki/frc-git-training/assets/77950550/71c074bf-46de-47cb-ae93-c7e5746fdaf1)

## What is squashing?
Squashing commits means merging multiple small commits that are all related into one big commit to contain all the features of the commits you squashed. This is used to clean up the hstory of your repository so there's no unnecessary commits that clutter up your history thus making it easier to browse through.
- For example, you just finished working on your code and you commited it but then you realized you had to change one of the variables and then has to commit that seperately. In this case you can squash it into the previous commit and have only one commit to represent both of those changes.
## Squash Commits
There is no `git squash` command, to squash you must use `merge` or `interactive rebase`.

### Squash through an interactive rebase
**Note:** You do not need to complete this by yourself but must know the commands for the practical as you will be asked to squash commits.
1. To squash multiple commits using interactive rebase, in your terminal type:

    ```git rebase -i HEAD~n```
    
    **Note:** The `-i` is used to enter interactive rebase and `HEAD~n` includes n commits from HEAD in the rebase.
2. A window should open with all the commits you selected. Change the first word from `pick` to `squash` for each of the commits except for the one on top(this is the commit where all the others will be merged to).
3. After closing the previous window another one will prompt you to enter the commit message, do so and close the editor window.
4. Finally you can push this commit using `git push`
