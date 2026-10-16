# Module 05: Package Feeds and Versioning

## Lesson Notes

Use GitHub Packages or Azure Artifacts for internal packages, feed permissions, upstream sources, and promotion views. Pin dependencies and prefer lockfiles. SemVer communicates compatibility (`MAJOR.MINOR.PATCH`); CalVer communicates date/order. Version pipeline artifacts immutably and record source commit, build/run ID, and provenance. Promote the same validated artifact instead of rebuilding between environments.

## Lab Notes

Inspect a local npm package:

```bash
npm pkg set name="@<scope>/az400-lab"
npm pkg set version="0.1.0"
npm pack --dry-run
npm pack
```

Create a private test feed in GitHub Packages or Azure Artifacts. Configure registry auth with the supported credential provider or pipeline service connection. Do not commit an `.npmrc` containing a token. Publish a test package to a development view, install that exact version from a clean consumer, validate it, and promote it to a release view if your plan supports views. Record package version, source commit, pipeline run, registry, and checksum/digest if available.

## Exercises

1. Choose SemVer or CalVer for a public SDK, internal build, and container image.
2. Define feed permissions for publishers, consumers, and release approvers.
3. Specify upstream-source policy, package promotion, dependency pinning, and retention.

## Verification

- A clean consumer installs the exact version from the intended feed.
- Package and artifact versions are traceable to source and pipeline.
- Release packages are immutable and cannot be overwritten by routine builds.
