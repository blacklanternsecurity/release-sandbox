# release-sandbox

A throwaway rehearsal of the BLS publishing release flow ([.github-config#16](https://github.com/blacklanternsecurity/.github-config/issues/16), policy in `.github-config` `docs/policy/publishing.md`). It is not a real package: it publishes `bls-release-sandbox` to **TestPyPI** only, and the repository will be archived once the rehearsal is done.

What it exercises:

- merge to `stable` → `release` environment approval by `bbot-leads` (not the person who merged) → TestPyPI through trusted publishing → `v*` tag and GitHub release created by the `bls-release` App;
- the release App's ID and key read from the `release` environment, with this repository's workflows passing nothing;
- an unchanged version releasing nothing, and a run from any branch but `stable` being refused;
- the `dev` gate: tests plus automated security checks, with authors merging their own `dev` pull requests.
