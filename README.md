Youth1.com Standard Operating Procedure
===

Git
---
* Commit messages should appropriately describe what is going into the commit.
* Commit modules as separate commits to other code with an appropriate message (e.g., "Adding XXX module.")
* Any new features should be committed as a separate commit, as should updates to features. I.e., keep adjustments to code separate from adjustments to features/modules.

Trello
---
* Make sure to @mention anytime something you add to Trello needs followup.
* Green flags mean an item is high priority. These should be done before any cards that do not have a green flag.
* If a Trello card has a Git commit associated with it, it should be linked to that commit using the GitHub integration
* Every Trello card should have a "deploy" checklist that includes steps that need to be taken to deploy that card.

CSS
---
* Use of `!important` should be kept to an absolute minimum. Any time you use `!important` you should add a comment as to why you put it there.

Commenting
---
* Comment anytime you do any of the following things:
 * Use `!important` in CSS
* Make sure to add a `TODO` comment anytime you commit code that should be reviewed later on.

Reviewing code
---
* Make sure comments occur anytime you see any of the following changes:
 * Use `!important` in CSS
 * A drush or other management command
 * A helper function whose purpose is not completely obvious by its title 
 * Any numbers are hard-coded vs. passed into a function as variables
* Look for any of the following potential security errors:
 * What are the permissions on any callback functions in hook_menu? Are they appropriately restrictive?
* Organization
 * Are all GUI changes included in an appropriate feature?
 * Are helper functions included as appropriate to simplify large blocks of code?
* Style
 * Is the code appropriately linted?

Deploying
---
* Make a database backup on LIVE before every deployment.
* Every Trello card should have a "deploy" checklist that includes steps that need to be taken to deploy that card.
* Github commits should include a comment containing the steps required to deploy the code (can be same as the deploy checklist on Trello)
* Any changes that can be inspected via a GUI should be deployed to a multidev branch so we can see and test them manually
