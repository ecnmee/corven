# Contributing to Corven

Thanks for your interest. A few things worth knowing before opening an issue or PR:

## Current status

Corven is pre-release. The Core (design tokens + atomic utilities) is being developed in a private monorepo. This repo doesn't accept code contributions yet — there's no stable public API to contribute against.

## What's welcome right now

- **Issues** describing bugs once the first release ships.
- **Discussions** about the approach, naming, or ideas — feedback is genuinely useful even pre-release.

## What's not welcome yet

- Pull requests adding new utilities, components, or features. Wait for the CONTRIBUTING guide to be updated once the public API is stable — this avoids work that gets thrown away if the API changes before v1.

## Naming and conventions

If you're proposing anything class-name or token related, it should follow the existing conventions: utilities have no prefix (`.flex`, `.p-4`), components use `c-`, layouts use `l-`, state uses `is-`. Familiarity with Tailwind's naming is a good baseline — Corven deliberately reuses it where there's no reason to diverge.

## Code of Conduct

By participating, you agree to abide by the [Code of Conduct](./CODE_OF_CONDUCT.md).
