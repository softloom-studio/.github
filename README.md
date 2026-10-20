# .github

Org-wide files for Softloom Studio.

- `profile/README.md`: public org profile.
- `.github/workflows/ios-build.yml`: reusable build + test + policy check for an app in `apps-ios`.
- `.github/workflows/ios-release.yml`: reusable TestFlight / App Review release (template, needs secrets).

Call from another repo:

```yaml
jobs:
  build:
    uses: softloom-studio/.github/.github/workflows/ios-build.yml@main
    with:
      app: MyApp
```

No secrets live here. Secrets are stored in each repo's GitHub Environments.
