# Gitflow 

## Summary 
Gitflow is a useful git framework helping developers to create features and correct bugs easily without breaking the app. It use the power of multi-branching development.

## Where to use it ?
At Innuendo we will use the gitflow protocol described in this file in  all repositories:
- innuendo-api
- innuendo-mobile
- innuendo-webapp

For all these repositories the workflow is the same.

## Main branches
In a repository there are thwo mai branches:

- main
- dev

### main
The `main` branch is where the production code is. Every push on `main` leads to a CI trigger that will deploy the code on the production server.

So this branch is very important and should only accept pushs from `dev` and **hotfix** branches.

### dev
The `dev` branch is step between **feature** branches and `main`. Every push on `dev` triggers tests CI in order to valid the code. It may also deploy on the staging server to have a preview of what will be deploy if we push `dev` code on `main`.

So the dev branch can accept pushs from **feature** branchs with the help of a [**pull request**](#pull-requests).

## Secondary branches
Secondary branches are temporary: you create them to fix/add/change some code and push it into `main` or `dev`.
There are two categories of secondary branches:

- hotfix
- feature

### hotfix
It is a branch directly created from `main` to correct a critical problem that is breaking the app. Normally it can not be a compilation or testing problem because all the code that has been pushed on `main` has been compiled and tested.

When you create a `hotfix` branch you must name it as follows:
```
hotfix/description-of-the-hotfix
```

You can merge it by creating a [**pull request**](#pull-requests).

### feature
A `feature` branch is created from `dev` and it change/add some code.

When you create a `feature` branch you must name it as follows:
```
<type>/description-of-the-branch
```

There are two `<types>` of `feature` branches:

- feat: add or change a feature(testing and documentation are always required for a new feature).
- fix: correction of a bug

You can merge it by creating a [**pull request**](#pull-requests).


## Pull requests
When creating a pull request for a branch, you ask for a review from the lead dev of the repository.

CIs of tests are triggered on the **pull request**. If tests are passing the lead dev can add comments on your code to discuss about it. When he think the code is well implemented he merge the **pull request** on the parent branch.

**You can never merge a branch without using a pull request**.