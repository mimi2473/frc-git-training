# squashing

## what is squashing?
Squashing commits means merging multiple small commits that are all related into one big commit to contain all the features of the commits you squashed. This is used to clean up the hstory of your repository so there's no unnecessary commits that clutter up your history thus making it easier to browse through.
- For example, you just finished working on your code and you commited it but then you realized you had to change one of the variables and then has to commit that seperately. In this case you can squash it into the previous commit and have only one commit to represent both of those changes.
## squash commits
There is no `git squash` command, to squash you must use `merge` or `interactive rebase`.

### squash through an interactive rebase
1. First navigate to `README.md` in your branch and add a second fact about yourself
2. Commit that change using `git commit` with the message:
    
    ```add second fact```
3. Add a third fact to `README.md` and commit it following step 2 but with the message:
    
     ```add third fact```
4. Now to squash these commits open the interactive rebase window using

    ```git rebase -i HEAD~2```
    
    **Note:** The `-i` is used to enter interactive rebase and `HEAD~n` includes n commits from HEAD in the rebase.
5. Finally a window should open with all the commits you selected. Change the first word from `pick` to `squash` for each of the commits except for the one on top(this is the commit where all the others will be merged to).
6. After closing the previous window another one will prompt you to enter the commit message, here change the commit message to:
    
    ```squashed fact 2 and 3```

    and close the editor window.
7. Finally you can push this commit using `git push`