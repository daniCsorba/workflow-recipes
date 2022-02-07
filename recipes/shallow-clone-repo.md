# Shallow clone the git repository

## Description

You can speed up the cloning of repositories by specifying clone depth. In case of pull request builds, you need to set the depth history to a number where both the source and destination branches are contained.

## Instructions

1. Set the **Limit fetching to the specified number of commits** input variable based on the build you are running:
    - If you run a build on a single branch, set it to `1`.
    - If you run pull request build, set it to a depth that contains both the source and target branches. For example, `100`. 

## bitrise.yml

```yaml
- git-clone@6:
    inputs:
    - clone_depth: 1
```

## Relevant Links

* https://discuss.bitrise.io/t/git-clone-step-is-very-slow/3844/2
* https://stackoverflow.com/questions/6941889/is-it-safe-to-shallow-clone-with-depth-1-create-commits-and-pull-updates-aga
