# SWR Contribution Guidelines

Thank you for reading this guide and we appreciate any contribution.

## Ask a Question

You can use the repository's [Discussions](https://github.com/vercel/swr/discussions) page to ask any questions, post feedback, or share your experience on how you use this library.

## Report a Bug

Whenever you find something which is not working properly, please first search the repository's [Issues](https://github.com/vercel/swr/issues) page and make sure it's not reported by someone else already.

If not, feel free to open an issue with a detailed description of the problem and the expected behavior. And reproduction (for example a [CodeSandbox](https://codesandbox.io) link) will be extremely helpful.

## Request for a New Feature

For new features, it would be great to have some discussions from the community before starting working on it. You can either create an issue (if there isn't one) or post a thread on the [Discussions](https://github.com/vercel/swr/discussions) page to describe the feature that you want to have.

If possible, you can add another additional context like how this feature can be implemented technically, what other alternative solutions we can have, etc.

## Open a PR for Bugfix or Feature

### Local Development

First of all, install dependencies and build SWR assets in watch mode:

```sh
corepack enable
corepack pnpm install

pnpm watch
```

To try your changes in a real Next.js app, run the e2e site in another terminal. It is a workspace package (`test/e2e/site`) with its own Next.js, installed by the step above, and it depends on `swr: workspace:*`, so it picks up the assets rebuilt by `pnpm watch`:

```sh
# http://localhost:4000
pnpm dev:e2e
```

### Before Opening a PR

Run the same checks as CI (`.github/workflows/test.yml`):

```sh
pnpm build
pnpm run-all-checks
pnpm test
pnpm test:build
```

## Update Documentation

To update the [SWR Documentation](https://swr.vercel.app), you can contribute to the [website repository](https://github.com/vercel/swr-site).
