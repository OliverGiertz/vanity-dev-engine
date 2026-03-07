# vanity-dev-engine

Shared CI/Security/AI reusable workflows for Vanity ecosystem repositories.

## Reusable Workflow

Use from another repository:

```yaml
jobs:
  use-vanity-dev-engine:
    uses: OliverGiertz/vanity-dev-engine/.github/workflows/repo-pipeline.yml@v1.5
    with:
      repo_type: ios
      xcode_project: CamperLogBook.xcodeproj
      xcode_scheme: CamperLogBook
```

## Inputs

- `repo_type`: `ios`, `node`, `python`, `custom`
- `xcode_project`: Xcode project path for iOS repos
- `xcode_scheme`: Xcode scheme for iOS repos
- `lint_command`: optional override
- `build_command`: optional override
- `test_command`: optional override

## Produced checks

- `use-vanity-dev-engine / ci`
- `use-vanity-dev-engine / security-scan`
- `use-vanity-dev-engine / ai-review`

## Consumer toggle

Set repository variable `USE_VANITY_DEV_ENGINE=true` in consumer repos to activate central execution.

Note: The default CI runner is `ubuntu-latest`. For iOS repositories, provide explicit `build_command` and `test_command` overrides (or use Xcode Cloud for build/test).
