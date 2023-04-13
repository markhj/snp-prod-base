[
  id: git-push-to-current
  tags:
  locations:
]: #

# Push current branch

Make ``git push <remote> <branch>`` into ``git push`` when you just want to push the branch you're on.

## Current repository
````bash
git config --local push.default current
````

## Globally
````bash
git config --global push.default current
````
