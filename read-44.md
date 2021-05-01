# Contributing to Open Source

To contribute to open source projects start by making a remote copy of the repository by forking it in Github.

Select the green button, in the repository window, labelled 'code' and copy the link shown in the dropdown menu.

Next move to making a local copy on your machine by opening your terminal window, navigating to the directory you wish to hold the repository, and running the command `git clone <url>` passing in the url in place of `<url>`.

Create a seperate working branch with `git checkout -b "<branch_name>"`, open the repository in your preferred code editor, and make the necessary changes.

When you're done adding your changes stage them for saving with `git add <directory_containing_changes>`, save them with `git commit -m "<few_word_explanation_of_changes>"`, and push them to this branch in the local repository with `git push origin <branch_name>` (you can also do this step before you finish to make sure your changes aren't lost in the event you lose your machine or the data on it).

If you're sure you don't need to make any more changes make a pull request to your main branch in Github. Start by clicking the word branches to the far left of the green code button from earlier. Find your working branch in the 'active branches' list (unless you made and pushed multiple branches it should be the only on in that list) and click the button to the far right of that line labelled `pull request`. Make sure the left drop down near the top says that it is merging to the open source project for this step. Add a merge message describing the changes in more detail, scroll to the bottom of the page to find the button labelled commit changes. When you click it it will show another button labelled 'merge' in order to make sure that's what you want. Go ahead and click both. When it's done complete another pull request changing the left drop down near the top to merge to you main/master branch.

That's it you're done.