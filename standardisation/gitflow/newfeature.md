# New feature

# Summary
This is the guide on how to add a feature on the codebase of any Innuendo repository.
This guide is called `new feature` but the same advices applies to a `fix` or a `hotfix`. Just adapt them to the context.


# Guide
## Starting with the ticket
A ticket is asigned to you and you decide to implement it.
Read the description and the checklist carefully to be sure it is pertinent and realisable (yes, team members are human and can do mistakes).

Just move the ticket in `In progress` bucket.

## Step 1: Creation of the branch
You need to create the branch, but first you need to by update with `main`:
```
git checkout main
git pull origin main
```

Then you can create your branch with a [correct name](gitflow.md/#feature):

```
git checkout -b feat/create-login-page
```

Nice ! You can start doing magic with your developer's hands !

## Step 2: During development
Don't forget to commit frequently, take a look at [this guide](../commits.md) to be a commit master.

Normally it is in the checklist but if not, you must provide some documentation of your code and some tests.

## Step 3: creation of the pull request
Now the feature is implemented and your code tested and documented. Is is time to ask the lead dev for a pull request.

Just push your code:
```
git push
```

And go on you repository on [Github](https://github.com).
A message should appear, click on `compare and pull request`.

Here you can add comments and ask a review of your lead dev.

When the lead dev authorize the merge of your branch you should have a notification by email.

Now you can move your ticket in the `complete` bucket.

Well done ! You pushed your first feature on the code base !