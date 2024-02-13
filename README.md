# Github Action to sync a public repo to a private repo

![002](https://github.com/stavares843/sync-public-repo-to-private-repo/assets/29093946/b5ccfa8f-5851-44a5-ae0d-d96f90f5d1f2)


# Description

If you have a public repo and want to test something with the same content on a private repo, you can do a private repo by
- Create a new repo
- Import the repo using the public URL
- You now have a private repo with the same content as the public one, but it's not synced automatically, and it doesn't have a sync button like the forked repos 
- Add the above file as a workflow and update it with the correct repo info
- Go to actions, select the action, click on run workflow, and run the action
- When you add a new commit on the public repo, re-running the action will update the branch on the private repo with the latest commit as well
- You can also add a cron job on the action to update automatically instead

# Usage


https://github.com/stavares843/sync-public-repo-to-private-repo/assets/29093946/a991ce55-6f4f-4dce-b7b4-4559c37340b0

<p align="center">
   <a href="/LICENSE"><img src="https://img.shields.io/badge/license-MIT-green.svg?style=flat" /></a>
</p>


# Notes

If your repo has a `.workflows` folder you need to add the following to avoid this error

<img width="713" alt="Captura de ecrã 2024-02-13, às 16 37 54" src="https://github.com/stavares843/sync-public-repo-to-private-repo/assets/29093946/feeafdd8-f216-486f-b65f-4e534bd8507a">

- You need to create a token with `contents:write` and `workflows:write` scopes and add it on the checkout step

```
      - name: Check out code
        uses: actions/checkout@v4
        with:
          # Fine-grained PAT with contents:write and workflows:write scopes
          token: ${{ secrets.WORKFLOW }}
``` 
