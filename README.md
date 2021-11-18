# git-tools

My collection of Git scripts


### `git sync`

> **WARNING:** This script is experimental. Use it at your own risk.

Fully sync your local and remote branch with a given remote branch.

**Usage:**

For example, if you want to sync your `feature` branch with `upstream/main`:

```
git checkout feature
git sync upstream main
```

That will make your local `feature` and remote `origin/feature` branch identical to `upstream/main`.

### `git setup`

> **NOTE:** This is not exactly a Git script, because Git doesn't know anything about forks. Probably should be named `fork-setup`.

This script detects the parent repository of a cloned fork and sets the parent repository as the `upstream` remote. Also, enables
the fetching of pull requests.

```
git clone <your-fork>
git setup
git fetch upstream
git checkout upstream/pr/<pr>
```
