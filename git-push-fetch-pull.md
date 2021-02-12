<!--- 
Changes in this edit: 

 - Rearranged some content for narrative flow.
 - Changed phrase to reflect that most users confuse git fetch and git pull 
   (not git pull and git push). 
 - Changed narrative to active voice, second person, present tense.
 - Changed "master" to "main" because that's what I see in the homework 
   given to me. If "master" is still is used, I'd propose an inclusive language
   section in the style guide. 
 - Replaced hyphens with en dashes in list items.
 - Replaced colons with different phrasing and/or split into separate sentences. 
 - Standardized content to plain English
 - Lowered reading level from 9th grade to 6th grade.

Suggestions:

 - The "Think of it as" sentence in the Push section makes the concept 
   clear. I love it. What do you think about adding a similar sentence in the
   Fetch and Pull sections?
 - We have some concepts, like tracking branch, that aren't used in a lot 
   of Git shops. Should we add a link for more information? Or do you 
   think our audience will understand?   

Note that nothing is written in stone. Feel free to call me for clarification. If any of my proposed edits changed your intended meaning, disregard my suggestion, accept my apologies, and claim a "get out of jail free" card to sucker-punch me after the pandemic.

--->

# What is the difference between push, fetch, and pull?

This topic defines some common Git commands used to work with remote repositories.  

## Push

`git push` checks whether your current branch is a tracking branch for a remote repository. If it's current, the changes in your local branch are pushed to the remote branch. This is how you share code with a remote repository. Think of it as _make the remote branch look like my local branch_. 

If your local branch doesn't have all the commits in the remote branch, `git push` fails. To resolve, synchronize your local branch with the remote branch. To synchronize, use either `git pull` or `git fetch` and `git merge`.

## Fetch

`git fetch` checks whether your current branch is a tracking branch. If it's current, Git pulls changes from the remote branch into the tracking branch. Your local branch does not change. To update your local branch, merge the changes by using `git merge origin/main`. (Replace `main` with whatever branch you want to update.)


## Pull

`git pull` is like `git fetch` but also merges any changes into your local branch. `git pull` does a `git fetch` followed immediately by `git merge`. This is usually what you want to do. Some people prefer to manually use `git fetch` followed by `git merge`. This helps them understand the changes they are merging into their local branch.

## Summary

- `git push` – send changes from a local branch to a remote repository
- `git fetch` – get changes from a remote repository into your tracking branch
- `git pull` – get changes from a remote branch into your tracking branch and merge them into a local branch

