# demo-webapp-npm

A public demo for [Stacklib](https://stackat.dev), the npm side of Stackat: a real React application, kept behind on
its dependencies on purpose, so you can watch Stacklib open its upgrade issues and pull requests in the open.

The application is [shadcn-admin](https://github.com/satnaing/shadcn-admin) by Sat Naing, at its release v1.4.0
(25th May 2025), under the MIT licence in [LICENSE](LICENSE). Nothing in its code was changed here. Its own README is
[UPSTREAM-README.md](UPSTREAM-README.md), and the current version lives in the original repository.

## What happens here

- Stacklib reads `package.json`, `pnpm-lock.yaml` and the source files, finds every npm package that is behind, and opens
  one issue per package with the breaking changes between this version and the latest, pointing at the lines of code
  they may touch.
- The issues are written by the GitHub App Stackpaw Dependencies and stay open until the package is upgraded.
- The dependencies are never upgraded on purpose: this repository stays behind so the issues keep showing what Stacklib
  finds.

Questions: support@stackat.dev
