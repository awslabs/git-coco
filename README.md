# git-coco

git-coco is a plugin for git that makes it easier to work with [AWS CodeCommit](https://aws.amazon.com/codecommit/) repositories.

## Usage

To use git-coco, just make sure it's in your path somewhere (either by copying it to somewhere like `/usr/local/bin` or adding the `git-coco` folder into your PATH variable).

The following commands are added to git:

* `git coco ls`

List all CodeCommit repositories.

* `git coco create <repo>`

Creates a new repository in CodeCommit and outputs the clone url.

* `git coco clone <repo>`

Clones the named repository from codecommit and configures it correctly for use with the [CodeCommit git credential helper](https://docs.aws.amazon.com/cli/latest/reference/codecommit/credential-helper/index.html).

* `git coco rm <repo>`

Removes the named repository from CodeCommit.

* `git coco init <repo>`

Performs the equivalent of a `git coco create` followed by `git coco clone`. The result is a checked out copy of a new CodeCommit repository

* `git coco pr <from> <to>`

Creates a pull request for the current repository that compares `<from>` (or the current branch if omitted) with `<to>` (or `master` if omitted).

* `git coco prlist <repo>`

Lists all open pull requests for a specified repository. Pull request information includes:
- Pull Request ID
- Pull Request Title
- Pull Request Merge Status
- Pull Request Destination Branch
- Pull Request Source Branch
- Pull Request Author
