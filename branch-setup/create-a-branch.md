# Branches 🌿

## What is a branch? 🤔
When you want to work on a certain part of a project (e.g new feature), instead of working directly on `main`, it's wiser to create another branch and later merge into main (or cherry-pick commits from your dev branch onto the main branch) once you have fixed any bugs with the new feature. This helps us keep the main branch clean and free of any issues.
- This is the most common practice in robotics, as you will see many of the projects that we will work on are developed in seperate test branches, and only merged into main if they are meant to be used for the final robot codebase.

## Create a branch + navigate to it! 🔀
1. Make sure you are on the master branch by entering `git checkout master`, this will navigate you to the master branch(use `git checkout <branch-name>` to navigate to different branches.)
2. Then to create the branch use `git branch git-training-first_name-last_initial`
3. Great!! you just created your first branch. the next you will learn how to stage and commit changes and how to push them to the branch.

## Stage, commit changes to branch... :arrow_up:
1. Navigate to the branch you just created. (hint, `git checkout`!)
2. Travel to *README.md* and enter in the information as specified. 
3. Run `git status` to see the status of the files. since you have not staged any file changes yet, it should not report any file changes. 
4. When you've done so, **stage** the commit with the command `git add <file>...` (this is used to track new untracked files, modified files, or deleted files).
   - Staging files seperately can help you commit only the files that are ready. if you want to stage ALL file changes, you can run `git add .` -- this is typically not advised for larger scale projects though.
5. Run `git status` again - you will now see that your changes to *README.md* will be registered and ready to be *committed.*
   - If you want to UNSTAGE a file, you can run the command `git reset HEAD <file>...`. 
6. Run `git commit -m <message>` to commit all the staged changes. 
    - Reminder to follow proper ettiquete in commit messages. 
    - `"(add/remove/delete) <present tense statement of what change you made>"`
7. Now add a new file in 📁: /branch-setup, called `new-file-first_name-last_initial`.
8. Stage the newly created file and commit ! (steps 4-6)
> [!NOTE]
> To write the commit message follow the instructions in this article on [How to Write Commit Messages](https://cbea.ms/git-commit/)
9. Now write the name of your first pet that you know in the file. (or anything that is workplace friendly should be fine - the content of the file is unimportant for the exercise)
10. Stage the changes to the file and commit. (steps 4-6)
11. Now write the name of your favorite restaurant that you know in the same file on a new line. (or anything that is workplace friendly should be fine - the content of the file is unimportant for the exercise)
12. Stage the changes to the file and commit. (steps 4-6)


If you have completed everything in this document, you are set up for the practical. 
Please take a close look at the prs.md, squashing.md, and cherry-and-tagging.md tutorials before arriving at the practical.
- As a reminder, the only document you're allowed to have open during the practical is the test-cheat-sheet.md. Though we will guide you throughout the process, we implore you to know what you're doing. competition day, you may not have time to look everything up you need to within games :grin:
