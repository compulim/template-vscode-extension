# template-vscode-extension

Template for creating Visual Studio Code extension.

## How to set up your new repository

1. [Click here](https://github.com/compulim/template-vscode-extension/generate) to use this template to create a new repository
1. Wait until the repository preparation is done
   - [Click here](../../actions/workflows/set-up-scaffold.yml) to check the progress of the workflow
1. [Click here](../../community/license/new?branch=main&filename=LICENSE) to create a `LICENSE` file
1. Create 2 new environments: `production` and `prerelease`
   1. [Click here](../../settings/environments/new) to create a new environment named `production` and `prerelease` respectively
   1. Add an environment secret named `VSCE_PAT`
   1. Paste your personal access token
      - Follow [this article](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=Windows) to create a personal access token
      - For permissions, make sure "Marketplace" > "Publish" is checked.
   1. (Optional) Protect your `production` environment by requiring approvals from collaborators

## How to publish

To publish, you need to push a tag that is corresponding to the version you want to publish. If you want to publish `0.0.1`, push a tag `v0.0.1` to your repository.

You can follow our steps:

- Assumptions
   - Your current version is `0.0.1-0` (pre-release of `0.0.1`)
   - You want to release `0.0.1`
- Steps to release
   - `git log` and make sure you are on the commit you want to publish as `0.0.1`
   - `npm version 0.0.1`
   - `git push -u origin v0.0.1`, this will trigger publish
- Post-release steps
   - Immediately after publish, bump to `0.0.2-0` by creating a pull request
   - `git checkout -b bump-0.0.2-0`
   - `npm version --no-git-tag-version prepatch`, this will bump to `0.0.2-0`
   - `git commit -a -m "0.0.2-0"`
   - `git push -u origin bump-0.0.2-0`
   - `gh pr create`

## Contributions

Like us? [Star](../../stargazers) us.

Want to make it better? [File](../../issues) us an issue.

Don't like something you see? [Submit](../../pulls) a pull request.
