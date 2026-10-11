# .github

Default community health files shared across personal repositories.

GitHub uses these files for any repository that does not have its own version in its root, `.github/`, or `docs/` directory. See [Creating a default community health file](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file).

## Templates

| File | Purpose |
| --- | --- |
| [pull_request_template.md](pull_request_template.md) | Default pull request description |
| [ISSUE_TEMPLATE/bug_report.yml](ISSUE_TEMPLATE/bug_report.yml) | Bug report form (`bug` label) |
| [ISSUE_TEMPLATE/feature_request.yml](ISSUE_TEMPLATE/feature_request.yml) | Feature request form (`enhancement` label) |
| [ISSUE_TEMPLATE/task.yml](ISSUE_TEMPLATE/task.yml) | Chore, refactor, docs, and other work items |
| [ISSUE_TEMPLATE/config.yml](ISSUE_TEMPLATE/config.yml) | Issue template chooser settings (blank issues allowed) |

A repository with its own `ISSUE_TEMPLATE` directory does not inherit any of these issue templates; the directory replaces them as a whole.

Labels are applied only if they exist in the repository. `bug` and `enhancement` are GitHub's default labels.

## pre-commit

[.pre-commit-config.yaml](.pre-commit-config.yaml), [.markdownlint-cli2.yaml](.markdownlint-cli2.yaml), and [mise.toml](mise.toml) are copied from `shared-config`. With mise installed, set up the tools and Git hooks:

```bash
mise install
mise exec -- pre-commit install
```

`pull_request_template.md` starts with a `##` section, so it disables MD041 (first line heading) with an inline comment instead of changing the shared markdownlint config.
