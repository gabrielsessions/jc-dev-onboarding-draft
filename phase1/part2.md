# Phase 1.2: Push, Pull, Commit, Branch

Let's start working with Git! Here's what we'll do:
  * Clone an Existing Repository
  * Create new branches
  * Stage and Commit changes
  * Pull/Push Changes
  
## Cloning the Starter Code
In a command line, change directories to a folder where you'd like to place the starter code. To clone the starter code for this phase run the command below. This will copy all of the reporsitory files and commit history to your local machine.

    git clone https://github.com/gabrielsessions/onboarding-2024-phase1.git


## Creating a new branch
In general, don't commit changes directly to the main branch. Create a new branch off of main whenever you have new changes to add. Here's the general process on how to create a new branch:

    git checkout main # Changes branch to main
    git pull # Pulls down latest changes on main
    git checkout -b my-branch-name # Create your new branch off of main

## Committing Changes
In your newly created branch, open up a code editor and create a new .txt file with your name. Include a fun fact about yourself in the txt file! Once you've saved the file with a fun fact, stage and commit your new file to the branch:

    git add . # Stages all files for a commit
    git commit -m "Your commit message here: Describe changes made to the codebase'

If all goes well, your changes will be committed locally. Now we need to push these changes to GitHub (remote).

    git push
    # The first time, this will likely spit back
    # a command that's \`git push --set-upstream ...\`.
    # Just copy and run that, it's a one-time thing.

Pushing to GitHub will require you to authenticate. Check out Ben's handy guide if you'd like to set up personal access tokens for authentication: [https://jumbocode.ben.page/reference/git-local](https://jumbocode.ben.page/reference/git-local)