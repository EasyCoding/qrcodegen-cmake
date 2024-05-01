# Contributing

This document describes how you can contribute to qrcodegen-cmake. Please read it carefully.

## Issues

Feel free to open issues, report bugs, request new features, or ask questions about our project.

## Pull requests

 1. Create your own fork by clicking the **Fork** button.
 
 2. Clone your fork's repository:
 ```bash
 git clone git@github.com:YOURNAME/qrcodegen-cmake.git
 ```
 
 3. Create a new feature branch `new_feature` and switch to it:
 ```bash
 git checkout -b new_feature
 ```
 
 4. Commit your changes:
 ```bash
 git add . && git commit -sm "Full description of your changes"
 ```
 
 5. Add the upstream as a [remote repository](https://help.github.com/articles/configuring-a-remote-for-a-fork/):
 ```bash
 git remote add upstream https://github.com/EasyCoding/qrcodegen-cmake.git
 ```
 
 6. Fetch changes from the upstream and [sync](https://help.github.com/articles/syncing-a-fork/) your fork's `master` branch with it:
 ```bash
 git fetch upstream
 git checkout master
 git merge upstream/master
 ```
 
 7. Rebase your feature branch to the updated `master`:
 ```bash
 git checkout new_feature
 git rebase master
 ```
 
 8. Squash all your commits into one and open a new pull request.

### Signing off your work

Don't forget to sign off your work by using `git commit -s`:
```
Signed-off-by: Name Surname <username@example.org>
```

We cannot accept pull requests with unsigned commits. We need this to upstream our work in the future.

### Some important warnings

 * Don't mix different line endings.
 * Don't upload any binary files to the repository.
 * Don't add and upload any temporary files.
 * Don't split CMake project file.
