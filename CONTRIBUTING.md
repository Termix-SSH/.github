# Contributing

Thanks for helping out. This is the default guide for every Termix-SSH repo. If a repo has its own `CONTRIBUTING.md`, follow that one instead.

## Before you start

- Check the open issues and pull requests first so you don't duplicate work.
- For anything bigger than a small fix, open an issue first so we can agree on the approach.
- Security problems go through the Security tab, not issues. See [SECURITY.md](https://github.com/Termix-SSH/.github/blob/main/SECURITY.md).
- Translations are done on [Crowdin](https://docs.termix.site/translations), not through pull requests.

## Setup

You need [Node.js](https://nodejs.org/en/download/) (the version in the repo's `.nvmrc`), npm and Git.

```sh
git clone https://github.com/Termix-SSH/<repo>
cd <repo>
npm install
```

`npm install` also sets up the Git hooks. They format your staged files with Prettier and check your commit message.

## Making a change

1. Fork the repo and create a branch from the default branch.
2. Make your change and add or update tests where the repo has them.
3. Run `npm run format`, and `npm run test` and `npm run lint` if the repo has them.
4. If the repo has a `CHANGELOG.md`, add your change under the next version.
5. Commit with a short message that starts with a type, like `feat: add host tags` or `fix: keep the sidebar open`.
6. Open a pull request with a clear description and link any related issues.

## Code style

- Follow the code around your change. Prettier handles formatting.
- Keep comments short and only where they help.
- Don't hardcode text in the UI. Use the translation files.

## Getting help

Ask in the [Discord](https://discord.gg/jVQGdvHDrf) or see [SUPPORT.md](https://github.com/Termix-SSH/.github/blob/main/SUPPORT.md).
