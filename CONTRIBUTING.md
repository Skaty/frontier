# Contributor's Guide

This document outlines the following:
* Basic guide on how to contribute to this repository
* Guidelines and Conventions for various aspects of this repository

## A. Beginner's Guide to Contributing

### Step 1: Set up the repository

Fork [this repository](https://github.com/NUSComputingDev/frontier) on GitHub to your own account and clone it to your development environment.

```
$ git clone <HTTPS/SSH URL of YOUR REPOSITORY>
```

Ensure that the remotes on your local repository contains the upstream repository. `upstream` is currently defined as `git@github.com:NUSComputingDev/frontier.git`

```
$ git remote add upstream git@github.com:NUSComputingDev/frontier.git
```

### Step 2: Create a branch

All changes to be made should be made in a branch, not `master`. Create a new branch and checkout to that branch.

```
$ git checkout -b <YOUR BRANCH NAME> -t origin/master
```

Follow the branch naming conventions that are outlined in Section B Part II.

### Step 3: Make & Commit your changes

Changes made to the codebase would eventually be committed to the local repository.

This project defines a commit as a unit of "logical change". The commit should be able to stand on its own, without having to depend on other subsequent commits. As such, commits should never be trivial and on the other hand, they must also not be too large (i.e. multiple features/components changed per commit).

Commit messages should be meaningful and for the most part, it should never be a one liner. On top of that, each commit message should be signed off by the author (using the author's actual name and email address). Pseudonyms/anonymous contributions are not allowed.

```
# Make a commit with signoff
$ git commit -s
```

Refer to Section B Part III for guidelines on commits and commit changes.

### Step 3b: Update your branch with latest changes

During the course of development, the `upstream` repository may have been updated with new changes. Do ensure that you fetch and rebase (NOT merge) the changes to your current branch from time to time.

```
$ git fetch upstream
$ git rebase upstream/master
```

### Step 4: Push changes to your forked repository

For the maintainers to view your modifications, your code must be on available on a publicly accessible repository. As such, you will need to push the changes to the repository that you have created in Step 1.

```
$ git push origin <BRANCH NAME>
```

### Step 5: Submit a Pull Request

A pull request submitted to the `upstream` repository would inform the maintainers that your changes should be considered added to the main repository.

Create a Pull Request on GitHub. The branch to merge to would depend on the type of patch that is being submitted. Non-critical bugs and feature patches should be merged to `develop`, while critical bug patches should be merged to `master`.

Refer to Section B Part IV for the guidelines and conventions on Pull Requests (e.g. message).

### Step 5b: Resolve Concerns

While the maintainers do not want to drag the pull request process too long, please note that there might be concerns/issues/questions raised by maintainers or other contributors.

In that case, the pull request will not be accepted until those concerns are resolved by you.

Any changes that needs to be made **MUST NOT** be done in a new commit, unless it is a separate, unrelated change. As commits denote a logical change, you will need to rebase and amend the appropriate commit. [Click here for a guide on rewriting history.](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History)

### Step 6: Accepted!

Hopefully your patch and pull request has been approved by the maintainers.

By allowing your signed changes to be merged to the main repository, you have certified that your contribution abides by the Developer's Certificate of Origin, which is included in Section C of this document.

## B. Guidelines & Conventions

All contributors should adhere to the following guidelines. The maintainers of the repository reserve the right to reject/ignore any contributions that do not adhere to the guidelines.

### i. Code Standards

* The [AirBnB style](https://github.com/airbnb/javascript) is the ES6 coding style that is adopted by this repository
* The EditorConfig file contains rules on how to format certain files
* There are no strict guidelines for other aspects of the project, but common sense must be exercised (e.g. directory structure, level of abstraction)

### ii. Branch Naming

* Branch names need to be singular
* It should describe the overall change for the patch that is to be submitted

### iii. Commit

* Each commit should record a *logical change* and not something trivial (e.g. fixing typo)
* Signoffs (`-s` flag) are MANDATORY and real names and email addresses must be used
* One liner commit messages are HIGHLY DISCOURAGED
* **Commit Summary (1st line)**
  * Limit it to 50 characters
  * Must be in the form -- <component> : <summary> (e.g. "ci: fix trailing spaces")
* **Commit Body (3rd line onwards)**
  * Limit to 50 characters per line (hard wrap each line)
  * Summarise the intent of the patch and the reasoning behind implementing it

Commit message example:
> about: modify font size for name headers
> The header font sizes need to be larger, to
> distinguish it from the description text of the MC
> member.
> <blank line>
> Sign-off-by: John Doe \<johndoe@example.com>

### iv. Pull Request

* Pull requests should be of appropriate size (in terms of logical changes made)
* Summarise in point/checklist/single sentence format the changes to be made in the patch
* Add appropriate labels and assign appropriate reviewers for the request
* Pull requests are considered dormant after ONE week and would not be considered after ONE month from the last activity related to the pull request

## C. Developer's Certificate of Origin 1.1
By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.