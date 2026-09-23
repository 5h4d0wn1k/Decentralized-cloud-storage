# Contributing to 5h4d0wn1k/5h4d0wn1k

Thank you for wanting to improve this profile repository. The goal is a
**professional, maintainable repo where every change makes the baseline better,
never worse.** The rules below keep it that way.

## Golden rules

1. **No direct pushes to `main`.** Every change ships through a PR, even one-line
   fixes. `main` always stays green and deployable.
2. **One concern per PR.** A bug fix, a section, or an automation change — not a
   mix.
3. **Verify images before you open the PR.** Every image/badge URL in the README
   must return `HTTP 200`. The CI workflow validates this automatically; don't
   force it to fail.
4. **Never reintroduce dead services.** `github-readme-stats.vercel.app`
   (503) and `github-readme-activity-graph.vercel.app` (402) are dead. Use
   verified alternatives (see README Analytics section).

## Workflow

1. Open an issue describing the change (bug, feature, or setup).
2. Branch from `main`: `git checkout -b fix/xyz` or `feat/xyz`.
3. Make the smallest meaningful change. Self-review the diff before committing.
4. Open a PR with the PR template filled out and link the issue.
5. CI runs the `README Health Check` workflow — all URLs must pass.
6. Review, then merge. Delete the branch after merge.

## Commit style

Use conventional commits so history stays readable:

```
fix(readme): repair dead capsule-render URL
feat(about): add CuboidSoft technical-lead role to experience
ci(healthcheck): validate all badge URLs on PR
```

## Style

- Keep alignment/section structure consistent (tables, centered blocks).
- Prefer verified, cached badge services over dynamic ones.
- Preserve the dark slate + cyan `#22d3ee` theme.