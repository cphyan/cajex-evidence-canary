# cajex-evidence-canary

A public canary repository for **cajeX Live Evidence**. cajeX reads it through
GitHub's read-only MCP server to test its checks against real GitHub answers.

Some things here are wrong **on purpose**, so the checks have something to find:

- `package.json` pins old versions of `lodash` and `minimist` with known
  advisories, so Dependabot raises real alerts. Nothing is built or run.
- `.github/workflows/ci.yml` has no security scanning and pins an action to a
  tag rather than a commit SHA.

`main` is protected by a ruleset that requires one approving review.
