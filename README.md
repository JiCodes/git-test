The git push command is used to update remote branches with your local commits. When you run git push origin, you are telling Git to push the local branch you're currently on to a branch with the same name on the remote repository called "origin."
Here's a breakdown of how it works:
- Local Branch: You are on a specific local branch (e.g., feature1) that contains your commits.
- Remote: origin is just a shorthand name for the URL of the remote repository where you want to push your changes. Typically, origin points to the remote repository from which you cloned your local repository.
- Branch Mapping: Git maps your local branch (e.g., feature1) to the corresponding branch on the remote repository (e.g., origin/feature1). This mapping is done automatically when you clone a repository or create a new branch.
- Push: When you run git push origin, Git sends the commits that are on your local branch but are missing on the remote branch to the remote repository.
- Update Remote Branch: If the remote branch (origin/feature1) doesn't exist, Git will create it. If it does exist, Git will update it with the new commits from your local branch.

So, when you mistakenly pushed your changes using git push origin main, Git pushed your local main branch to the remote main branch, but it didn't remove your local feature1 branch or its commits. Your feature1 branch and its commits were still intact in your local repository.

When you subsequently pushed your feature1 branch to origin/feature1 using git push origin feature1, Git correctly updated the remote feature1 branch with the commits from your feature1 branch.