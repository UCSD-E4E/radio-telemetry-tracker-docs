# GitHub Guidelines

If you will be contributing to our codebase, you should have completed the git/GitHub training form. Make sure you understand the processes covered in this training and what mistakes you made. Here are some additional tips and expectations in our shared GitHub repositories:

### Creating new branches:
The training form went through creation of a new branch, but here is a brief review:

Navigate to the appropriate base branch by checking it out. This might be main/master if you are creating a new feature, or it could be a feature branch if you are contributing to the same feature branch as other team members, for example.

Create your new branch. Give it a name which succinctly summarizes its purpose, and add your initials at the end of the name. For example, John Doe making a branch for the feature "foo" would name the branch `foo_JD`.

Checkout your new branch so your changes appear on that branch.

### Commits:
You probably know how to commit changes already, but it's also important to know *what* to include in each commit (it isn't "everything I want to change").

In general, it's best to make several small, targeted commits which each handle their own new feature or bug fix, rather than making one big commit which changes several unrelated things at once.

Your commit message should communicate the small change(s) you made, more than their result or purpose. We want to be able to look through commit history to determine when any given segment of code was added, modified, or deleted; communicate these actual edits in your commit messages, and save explanation of the results for merges.

### Style:
Don't forget good style! For example, our Python repositories should adhere to PEP-8 standards. Make sure you understand what this means for file_names, ModuleNames, function_names, variable_names, import order, docstrings, and more. Don't forget to update documentation, including module docstrings, function docstrings, and READMEs, when you make changes which impact the information in that documentation.
It's recommended to install pylint for help with Python style. If pylint complains about anything, some effort should be made to correct it if deadlines allow.
Some of our code doesn't currently adhere to style guidelines. If you are able to improve these files in the course of your work, please do.

**See full style guidelines in this repo's `style_guides` folder.**

### Merges:
When you are done with a feature or bug fix and are ready to merge it into the base branch, make sure you've followed these steps:
1. Resolve merge conflicts. Specifically,
	1. Checkout the base branch
	2. Pull any updates to the base branch so that your local copy is up-to-date
	3. Checkout your branch again
	4. Merge the base branch into your branch with `git merge <base_branch_name>`
	5. If there were no conflicts, you're done and can push your changes and continue to step 2. If there were conflicts, resolve them, commit your changes, and run any tests again to be sure everything functions as expected. Restart at (a) once your branch's version has been tested.
2. Request review from anyone who worked on the branch with you, plus the project lead.
3. Respond to any questions or concerns from your reviewers, and do not merge until your reviewers have approved the request. If you make further changes or the base branch receives updates before your merge is completed, repeat step 1.

If a review is requested from you, do your best to thoroughly review all the changes and provide comments on anything you would change. If you have no concerns, approve the request and keep an eye out for further discussion. Here's some advice if you're new to code review:
- Bear in mind the overall design changes or additions of this merge. If a feature adds a new class with ties to old classes, for example, you'll need to be careful in your review to consider not just the code for the new class but also how that aligns with existing code.
- Look out for easy-to-make errors like off-by-one errors, race conditions, or simple typos.
- Don't be afraid to be nitpicky! If a change ought to be made, call it out. If you don't, it'll crop back up as a bug later and be harder to track down.
- Take your time to thoroughly analyze each updated file.
- Remember to review style and request changes if the files to be merged don't adhere to our style guidelines.
