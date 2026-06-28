# Contributing to Orenva Health

Thank you for thinking about contributing.

This is the **organisation-wide default** contribution guide for
every repository under [Orenva-Health](https://github.com/Orenva-Health).
Where an individual repository has its own `CONTRIBUTING.md`, that
guide takes precedence for matters specific to that repo.

Most of our repositories are **private** because they hold product
code, infrastructure-as-code, or compliance evidence that includes
or references sensitive information. Public contributions are
welcome on the repositories that are explicitly public.

## Before you start

- Read the [Code of Conduct](./CODE_OF_CONDUCT.md). It applies to
  every interaction in this organisation's spaces.
- Read the [Security policy](./SECURITY.md). **Never** open a
  public issue or pull request for a suspected vulnerability — see
  the policy for the disclosure path.
- Check the repository's own README and any `CONTRIBUTING.md` for
  repo-specific setup steps, code style, and review expectations.

## What we welcome

- **Bug reports** — clear, reproducible, and scoped to a single
  problem. Include the repository, the environment (OS, browser,
  version), the steps to reproduce, what you expected, and what
  actually happened.
- **Feature requests** — describe the user problem first, then the
  proposed change. We are more interested in the problem than the
  specific solution; that helps us find the right shape.
- **Documentation improvements** — typos, broken links, unclear
  wording, missing examples. These are some of the highest-leverage
  contributions and we are grateful for them.
- **Pull requests** — please open an issue first for non-trivial
  changes so we can agree the approach before you spend time on it.

## What we cannot accept

- Pull requests that introduce code without tests where the
  repository already has a test culture
- Changes that touch authentication, billing, clinical-data flows,
  or third-party sub-processors without prior discussion — these
  must follow our Change Management policy
- Contributions that re-license code or add dependencies with
  incompatible licenses
- Contributions made in violation of the contributor's employer's
  IP-assignment terms

## How to open a pull request

1. **Fork the repository** (for public repos) or create a feature
   branch named `kind/short-description-YYYY-MM-DD` — e.g.
   `fix/login-redirect-2026-06-28`.
2. **Keep the change focused.** One concern per pull request. If
   you spot something else, open a follow-up issue rather than
   piling it into the same PR.
3. **Match the existing code style.** Look at the surrounding
   files; do not reformat unrelated code.
4. **Write a clear PR title and description.** Title in imperative
   mood ("fix the login redirect"), description covers *why* not
   just *what*, and links to any related issue.
5. **Run the local checks** the repository documents (typically
   `npm run lint`, `npm run typecheck`, `npm run test`, and a
   production build) before pushing.
6. **Be patient and responsive in review.** We aim to give an
   initial response within five business days; complex changes can
   take longer.

## Commit messages

Conventional, present-tense, one line of subject + optional body:

```
fix: stop the login redirect dropping the locale prefix

When a user signed in on /de-DE/login the redirect went to /
instead of /de-DE/. Honour the locale stored in the session.

Closes #123
```

Prefixes we use: `feat`, `fix`, `docs`, `refactor`, `test`,
`chore`, `perf`, `revert`, `style`, `ci`, `build`, `deps`.

## License and contributor terms

Unless a repository says otherwise, contributions to public
Orenva-Health repositories are accepted under the same license as
the repository they target. By opening a pull request you certify
that:

- The contribution is your own work, or you have the right to
  contribute it
- You agree it can be distributed under the repository's license
- You understand it may be modified, redistributed, or removed at
  any time

## Questions

- Public discussion: open a GitHub Discussion on the relevant repo
- General questions: `hello@orenvahealth.com`
- Security: see [SECURITY.md](./SECURITY.md)
- Conduct concerns: see [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md)

Last reviewed: 2026-06-28.
