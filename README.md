# update-changelog-action

> [!WARNING]
> This action is deprecated and will not be maintained anymore.
> Please use our [LizardByte/actions](https://github.com/LizardByte/actions) monorepo instead.

[![GitHub Workflow Status (CI)](https://img.shields.io/github/actions/workflow/status/lizardbyte/update-changelog-action/ci.yml.svg?branch=master&label=CI%20build&logo=github&style=for-the-badge)](https://github.com/LizardByte/update-changelog-action/actions/workflows/ci.yml?query=branch%3Amaster)

A reusable action to update a changelog, based on the contents of the GitHub releases.

## Basic Usage

See [action.yml](action.yml)

```yaml
steps:
  - name: Update Changelog
    uses: LizardByte/update-changelog-action@master
    with:
      token: ${{ secrets.GITHUB_TOKEN }}
```

## Inputs

| Name                   | Description                            | Default         | Required |
|------------------------|----------------------------------------|-----------------|----------|
| changelogBranch        | The branch to store the changelog in.  | `changelog`     | `false`  |
| changelogFile          | The file to store the changelog in.    | `CHANGELOG.md`  | `false`  |
| token                  | GitHub Token.                          |                 | `true`   |

## Outputs

| Name      | Description                              |
|-----------|------------------------------------------|
| changelog | The contents of the generated changelog. |

## See Also

This action is meant to be used in conjunction with
[LizardByte/setup-release-action](https://github.com/LizardByte/setup-release-action).
