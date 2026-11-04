# Contributing to Argowei

Thanks for helping improve Argowei. The main application lives in [argowei/argowei](https://github.com/argowei/argowei).

## Before you start

- Search existing issues and pull requests before opening a new one.
- For a larger change, open an issue describing the problem and proposed approach so the scope can be discussed.
- Keep changes focused. Explain the user-visible behavior and any network or deployment assumptions.
- Use the [security policy](SECURITY.md) for sensitive vulnerabilities instead of a public issue.

## Local checks

From the application repository root:

```bash
cargo fmt --all -- --check
cargo clippy --workspace --all-targets --locked -- -D warnings
cargo test --workspace --locked
cd frontend && npm ci && npm run build && npm test -- --watch=false
```

The API integration tests need PostgreSQL and a `DATABASE_URL`; see the [technical reference](https://github.com/argowei/argowei/blob/main/docs/TECHNICAL-REFERENCE.md#backend-checks). For documentation-only changes, check links and rendered Markdown.

## Pull requests

Describe what changed, why, and how you checked it. Include screenshots for visible dashboard changes. If a change affects deployment, configuration, permissions, or data migrations, call that out explicitly.
