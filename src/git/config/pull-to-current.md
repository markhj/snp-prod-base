[
  id: git-pull-to-current
  tags:
  locations:
]: #

# Pull current branch

Make ``git pull <remote> <branch>`` into ``git pull`` when you just want to pull the branch you're on.

## Current repository
````bash
git config --local pull.default current
````

## Globally
````bash
git config --global pull.default current
````
