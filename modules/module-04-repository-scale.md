# Module 04: Repository Scale, Large Files, and Git Recovery

## Lesson Notes

Git LFS stores large object contents separately while Git tracks pointers; `git-fat` uses implementation-specific external storage. Scalar helps scale large Git repositories. Cross-repository sharing choices include packages, submodules, and subtrees. Use tags for immutable releases. Recover with `git restore`, `git revert`, `git reflog`, and `git fsck`. Removing a secret requires immediate revoke/rotation; history rewriting is coordinated incident response and does not erase forks/caches/clones.

## Lab Notes

Track a harmless generated file with LFS:

```bash
git lfs install
git lfs track "*.bin"
git add .gitattributes sample.bin
git commit -m "Track sample asset with LFS"
git lfs ls-files
```

If Scalar is available, compare a clone:

```bash
scalar clone <repository-url>
scalar list
```

In a disposable repository, practice:

```bash
git revert <commit-sha>
git reflog
git switch -c recovery/test <reflog-or-commit-ref>
git fsck --lost-found
```

Use `git filter-repo --path test-secret.txt --invert-paths` only on a fresh disposable repository containing a fake marker, never a real credential or shared history.

## Exercises

1. Compare LFS, git-fat, Scalar, submodules, subtrees, and package sharing for large assets/libraries.
2. Write recovery procedures for an accidental reset, bad shared commit, deleted branch, and leaked secret.
3. Define repository permissions, tag naming, and large-file quotas.

## Verification

- LFS pointer resolves to its object.
- Shared mistakes use revert rather than destructive reset.
- Explain history-rewrite coordination and why credential rotation comes first.
