# gh-merge-dependabot

A Github CLI extension script to combine multiple dependabot pull requests into a single pull request. Based loosely on [combine-prs-workflow](https://github.com/hrvey/combine-prs-workflow).

## Installation

```bash
gh extension install matt-bartel/gh-merge-dependabot
```

## Usage

```txt
gh merge-dependabot [-n NAME] [--no-push] [--no-pr] [BRANCHES...]
  -n NAME
    Set the name of the generated pull request. Default: "chore: dependabot version updates"
  --no-push
    Do not push changes to the remote. This implies --no-pr.
  --no-pr
    Do not create a pull request.
  BRANCHES
    Optional space separated list of branches to combine. If this is not specified the script will use branches for every pull request opened by dependabot.
  -h, --help
    Display this message.
```

## Examples

Create a new pull request combining all open pull requests created by dependabot:

```bash
gh merge-dependabot
```

Create a new pull request combining remote branches `branch-1`, `branch-2`, and `branch-3`:

```bash
gh merge-dependabot branch-1 branch-2 branch-3
```
