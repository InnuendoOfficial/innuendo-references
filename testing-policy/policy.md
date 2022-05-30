# Testing policy

# Summary
Bugs and side effects are part of the developer journey. Moreover with scalable project like Innuendo developers can make mistakes.

To prevent bugs you have to implement a testing policy and follow it.
In this file you can find all the aspects of the Innuendo's testing policy.

Goals: 
  - prevent bugs and side effects
  - make sure a bug won't appears again
  - have a qualitative and clean codebase
  - have a scalable codebase

We want to test the feature first: functional tests are our priority and we want to use unit tests only for utility and logical functions (ex: a function that convert timestamp into DD/MM/YYYY formatted date).

# Functional tests
Functional tests are the most important, we want a platform that works well, not a codebase that passes all tests.

## When ?
As we want a functional product, all the **main** features have to be tested: all user stories must be covered.

In addition, when a bug appears it has to be covered.

## How ?
When you are implementing a new feature, make sure to note all the way the user can interact with it. Once it's done you can develop the multiple tests: normal cases, error cases, angry cases...

If you want to cover a bug, identify how to user triggered it and reproduce the story in the test.


# Unit tests
Unit test are secondary in our project. But they are very usefull when they cover strategic functions.

It concerns all the utility logical functions.

## When ?
From the moment you are writting a function that will be used more than one time, you have to control its output.

Also, when you are writting utility functions:
```
nbToString()
dateToFormat()
getMostOccurentLetter()
```

You need to test them.

## How ?
When you are implementing a function to test, try to think about all possible values that can be passed as parameter and write tests for them.

Then you can add guards in your function to prevent errors to occur.

Once it's done, ask you the question:
**What is the role of my function ?**.

For example the function ``getMostOcurrentLetter``:

```
getMostOcurrentLetter('here is sentence') -> e
getMostOcurrentLetter('aaaaa') -> a
getMostOcurrentLetter('ab') -> [a, b]
```

At this point you just need to write tests and make them pass.

WARNING: don't write tests for the code, write code for the tests.