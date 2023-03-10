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

### Create Release Candidate
```sh
$ git flow release start 1.0.1
```
The Above commands will trigger the below actions:
- A new branch 'release/1.0.1' was created, based on 'develop'
- You are now on branch 'release/1.0.1'
### Finish the Release Candidate
```sh
$ git flow release finish 1.0.1
```
The Above commands will trigger the below actions:
- Release branch 'release/1.0.1' has been merged into 'main'
- The release was tagged '1.0.1'
- Release tag '1.0.1' has been back-merged into 'develop'
- Release branch 'release/1.0.1' has been locally deleted; it has been remotely deleted from 'origin'
- You are now on branch 'develop'

Once release flow finish, Push the changes in local to remote, that includes git push from develop as well as main and then push the recently created git tags.
