# Commit convention

## Summary
We want to have a commit convention because it helps to have more understandable codebase and forces us to split tasks correcly. This convention is based on [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/#specification).

### 1. Commit structure 
All commits messages must be structured as follows:

```
<type>[optional scope]: <description>
```
example:
```
feat(login page): add info message when password is wrong
```

### 2. Types
there are several types that must be used in the right way:

- feat: a new feature
- fix: a bug fix
- refactor: a code change that neither fixes a bug nor adds a feature
- docs: documentation only changes
- test: adding missing tests or correcting existing tests

### 3. Optional scope
A scope can be added between parenthesis to add a context to the commit if the codebase is too large.

tips:
- For front-end apps you can use the page name as context 
- For back-end you can use the name of the route or the module

In order to have pertinent scopes you have to commit frequently (you can't add all files in a single commit if they are not in the same context).

### 4. Description
The description of the commit is very important. You should understand what a commit changes in the codebase by just looking at the description.

examples:

```
feat(login page): add login with google button
fix(login page): remove infinite loading if request fails
refactor(login page): split form in multiple components
```