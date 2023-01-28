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

1. Tag your commit with semver and prefix it with letter `v`, such as `v0.0.1`
1. Push the tag to GitHub

## Contributions

Like us? [Star](../../stargazers) us.

Want to make it better? [File](../../issues) us an issue.

Don't like something you see? [Submit](../../pulls) a pull request.
