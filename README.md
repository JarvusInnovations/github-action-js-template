# github-action-js-template

This repository is a template for any GitHub repository that needs to be published to a branch with `node_modules/` populated

It makes use of [`hologit`](https://github.com/JarvusInnovations/hologit) to declaratively configure the distributed form of the branch.

## Usage

To install into an existing project, just copy in the `.holo/` and `.github/` trees.

### Testing locally

```bash
npm install -g hologit
git holo project --working --commit-to=v1 github-action
```

### Configuration

There are a couple things you may want to tweak for your project:

- The globs list in `.holo/branches/github-action/_action-sources.toml` declares what tree content is included in distribution
- The workflow configuration in `.github/workflows/github-action.yml` declares what branch gets published from and where it gets published to
