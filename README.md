# vanity-dev-engine

Shared CI/Security/AI reusable workflows for Vanity ecosystem repositories.

## Reusable Workflow

Use from another repository:

```yaml
jobs:
  use-vanity-dev-engine:
    uses: OliverGiertz/vanity-dev-engine/.github/workflows/repo-pipeline.yml@v1.2
    secrets: inherit
    with:
      repo_type: ios
```

Optional inputs:

- `repo_type` (`ios`, `node`, `python`, `custom`)
- `lint_command`
- `build_command`
- `test_command`

Optional control:

- set repository variable `USE_VANITY_DEV_ENGINE=true` in consumer repos.
