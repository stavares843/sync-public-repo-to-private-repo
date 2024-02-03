# Github Action to sync a public repo to a private repo

![002](https://github.com/stavares843/sync-public-repo-to-private-repo/assets/29093946/b5ccfa8f-5851-44a5-ae0d-d96f90f5d1f2)


# Description

If you have a public repo and want to test something with the same content on a private repo, you can do a private repo by
- Create a new repo
- Import the repo using the public URL
- You now have a private repo with the same content as the public one, but it's not synced automatically and it doesn't have a sync button like the forked repos 
- Add the above file as a workflow and update it with the correct repo info
- Go to actions, select the action, click on run workflow, and run the action
- When you add a new commit on the public repo, re-running the action will update the branch on the private repo with the latest commit as well
- You can also add a cron job on the action to update automatically instead

# Usage

https://github.com/stavares843/sync-public-repo-to-private-repo/assets/29093946/cefb7cd7-711d-4305-840e-381ac979c486

