# Cloning the repository

## Description

Clone a Git repository.

## Instructions

1. Make sure you have the [Activate SSH key (RSA private key)](https://github.com/bitrise-steplib/steps-activate-ssh-key) Step in your Workflow. This allows the Git client on the build VM to access private repositories.
2. Add the [Git Clone Repository](https://github.com/bitrise-steplib/steps-git-clone) Step.
    - Check out the optional input variables in the Workflow Editor or in the Step documentation.

## bitrise.yml

```yaml
- activate-ssh-key@4:
    run_if: '{{getenv "SSH_RSA_PRIVATE_KEY" | ne ""}}'
- git-clone@6: {}
```
