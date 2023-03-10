# Gitflow Semver Demo
Example workflow for automatic semantic versioning with gitflow.

## Installation of git-flow

### Installing on Ubuntu/Debian - git should be the Prerequisite for this
```sh
$ sudo apt install git-flow
```
## Initialize/Enable the git flow Repo
```sh
$ git flow init
```

### Feature development and Release Process
```sh
git checkout develop
git pull origin develop
git flow feature start featureName
```

### publish/pull a feature to/from the remote
```sh
git flow feature publish featureName
git flow feature pull featureName
```
### Finish Feature - merge the feature branch into develop and remove it locally and remotely
```sh
git flow feature finish featureName
```

# test feature
