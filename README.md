# .github

Reusable workflows found in `.github/workflows`.
GitHub does not distinguish workflows that should run in this repository,
from reusable workflows that are expected to be called elsewhere.
The only way to tell is that reusable workflows include `workflow_call` event trigger.

## Releasing

Reusable workflows, like actions, should have a `vMajor` git ref 
such that consumers may pin to a fuzzy version and avoid receiving breaking changes.
To that end, the `tag-major` workflow will ensure a `vMajor` ref is kept up to date 
in response to pushed tags.

It is recommended in this repository to trigger a release by manually create a GitHub Release,
choosing the next version tag, and publishing (ideally using the generated release notes).
