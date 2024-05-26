# branches 🌿

## create a branch + navigate to it! 🔀
1. make sure you are on the master branch by entering `git checkout master`, this will navigate you to the master branch.(use `git checkout <branch-name>` to navigate to different branches.)
2. then to create the branch use `git branch git-training-first_name-last_initial`
3. great!! you just created your first branch. the next you will learn how to stage and commit changes and how to push them to the branch.

## stage, commit changes to branch... :arrow_up:
1. navigate to the branch you just created. (hint, `git checkout`!)
2. travel to exercise-setup.md and enter in the information as specified. 
3. run `git status` to see the status of the files. since you have not staged any file changes yet, it should not report any file changes. 
4. when you've done so, **stage** the commit with the command `git add <file>...`. (this is used to track new untracked files, modified files, or deleted files)
   - staging files seperately can help you commit only the files that are ready. if you want to stage ALL file changes, you can run `git add .` -- this is typically not advised for larger scale projects though.
5. run `git status` again - you will now see that your changes to exercise-setup.md will be registered and ready to be *committed.*
   - if you want to UNSTAGE a file, you can run the command `git reset HEAD <file>...`. 
6. run `git commit -m <message>` to commit all the staged changes. 
7. now add a new file in 📁: /branch-setup, called `new-file-first_name-last_initial`.
8. stage the newly created file and commit !

## fetch vs. pull
