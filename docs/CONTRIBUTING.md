# Contributing to \<Repo-Name>

First of all, :+1: **thank you for** :+1:  taking the time to read this and contributing to the project.

Due to the impact that the modification of the project may have, we have defined a governance model for this repository.

## Table of contents

- [Code of conduct](/#Code-of-Conduct)

- [How can I contribute?](#how-can-i-contribute)
  - [Repository Clone](#repository-clone)
  - [Make your own new branch](#make-your-own-new-branch)
  - [Publish your branch and changes](#commiting-changes-to-code)
  - [Generating new Pull Request](#generating-new-pull-request)


- [Styleguides](#styleguides)
  - [Git Repository Governance](#git-repository-governance)
  - [Git Commit Messages](#git-commit-messages)
  - [Documentation Styleguide](#documentation-styleguide)

## Code of Conduct

See [Code of Conduct](CODE_OF_CONDUCT.md)

## How can I contribute

### Repository Clone
Clon the repository from its URL with e.g. GitHub Desktop or GitBash

```
git clone https://github.com/antoniohernan/putfiles2ec2.git
Cloning into 'putfiles2ec2'...
remote: Enumerating objects: 39, done.
remote: Counting objects: 100% (39/39), done.
remote: Compressing objects: 100% (38/38), done.
remote: Total 39 (delta 10), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (39/39), 9.08 KiB | 2.27 MiB/s, done.
Resolving deltas: 100% (10/10), done.

```

### Make your own new branch
Creates a new working branch for your contribution from the main branch

```
git checkout -b <new_branch_name> <specific_different_branch>
```

Try to make the name of the new branch contain something to identify its purpose.

### Publish your branch and changes

We add our new branch and the changes we have made to github.com

Please review the best practices regarding [commit messages](#git-commit-messages).  

```
$ git push -u origin develop
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 4 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (10/10), 3.15 KiB | 645.00 KiB/s, done.
...
```

### Generating new Pull Request

You can create the new Pull Request using the URL shown by the publish command of the new branch. 
Pull Requests are carefully reviewed by the team in charge.
Issues will be generated as necessary to correct any deficiencies before accepting the changes and proceeding to merge them into the main branch.


## Styleguides

### Git Repository Governance

This repository is managed using Trunk-based philosophy:

| Git-flow | Trunk-based |
|---|---|
| As far as possible from main branch | As close as possible to main branch |
| New features started from develop branch | Short-lived feature branches started from main branch |
| New release branch derived from develop branch, after stabilized release branch deployed | Main branch always in a state ready to be deployed to production |
| Only hotfixes derived from main branch | Hotfixes start from main or release branch, need to be cherry-picked back to main |

Trunk Based Development allow feature branches as a tool for code review, with some restrictions:

- Feature branches are short-lived (shorter is better, definitely not more than a few days)
- Only one developer commits to a given feature branch.
- Feature branches branch from the trunk and can only be merged to the trunk.
- Merging from the feature branch to trunk is allowed only once and also means the end of the feature branch
- Merging from trunk to bring the feature branch up to date with new changes is allowed anytime. It is especially recommended to bring your feature branch fully up to date with the trunk (and check that it builds) before actually merging into trunk


### Git Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Avoid configuring non-HTTPS connections..." not "Avoids configuring non-HTTPS connections...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line

### Documentation Styleguide

TODO
