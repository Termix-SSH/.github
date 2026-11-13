# Security Policy

Termix holds the keys to the servers it manages, so we take reports seriously. Thank you for helping.

## Reporting a vulnerability

Please do not open a public issue, pull request or Discord post for a security problem.

Report it privately with Report a vulnerability on the Security tab of the repo the problem is in. For the server, the desktop app, or if you are not sure which repo, use https://github.com/Termix-SSH/Termix/security/advisories/new. Only you and the maintainers can see the report.

Please include:

- What is affected (server, desktop, mobile, CLI, plugin, release process) and the version you tested
- Steps to reproduce, ideally a short proof of concept
- What an attacker gains, and what access they need first

Machine readable contact: https://termix.site/.well-known/security.txt. Every Termix server also answers `/.well-known/security.txt`.

## What happens next

| Step                                         | Target                                                    |
| -------------------------------------------- | --------------------------------------------------------- |
| First reply                                  | 3 days                                                    |
| Confirmed or declined, with a severity score | 7 days                                                    |
| Fix released for critical and high           | 30 days                                                   |
| Fix released for medium and low              | 60 days                                                   |
| Advisory published                           | When the fixed version is out                             |
| Latest you may go public                     | 90 days after the report, unless we agree on another date |

These are targets for a small team. If we are going to miss one, we tell you in the advisory. We ask GitHub for a CVE for every confirmed problem and publish the advisory once users can update. Please keep the details private until then.

## Scope

In scope:

- The Termix server and its Docker images (https://github.com/Termix-SSH/Termix)
- The desktop app on Windows, macOS and Linux, including its updater
- The mobile app (https://github.com/Termix-SSH/Mobile) and the CLI (https://github.com/Termix-SSH/CLI)
- Every official plugin (`Termix-SSH/Plugin-*`) and the plugin SDK `@termix-ssh/plugin-sdk`
- The plugin sandbox: a plugin reaching anything it was not granted is a bug
- The plugin registry, plugin signing and the release workflows (https://github.com/Termix-SSH/Termix-Registry)

Out of scope:

- Community plugins. Report those to their author. A problem in how the registry checks or signs them is in scope
- Attacks that need admin rights on the Termix server, root on its machine, or a copy of its data folder and keys. Admins are trusted by design
- Plugins an admin chose to run with Run without isolation, beyond what the plugin itself gets wrong
- The demo at demo.termix.site, which runs in your browser on fake data
- Denial of service by sheer volume, spam, and social engineering of maintainers or users
- Missing headers, cookie flags or version banners without a working attack
- Scanner or AI tool output that has not been checked by hand
- Problems only in releases older than the latest one

## Supported versions

Only the latest release of the server, the desktop app, the mobile app, the CLI and each plugin gets security fixes. Please update before reporting.

## Safe harbor

If you act in good faith under this policy, we will not take legal action against you or report you to anyone for your research. Good faith means you:

- Only test against your own install or accounts you own, never someone else's server
- Stop as soon as you can show the problem, and do not read, change or delete other people's data
- Do not degrade the service for others
- Give us a fair chance to fix the problem before you share details

If something you want to try is not clearly covered, ask in the advisory first. If a third party takes action against you for research done under this policy, we will make it clear that you acted with our permission.

## Credit

You are credited in the GitHub advisory unless you ask not to be. Every reporter is also listed on the thanks list at https://docs.termix.site/security#thanks. Tell us in the report if you want a different name or link.

Termix is free and has no paid bug bounty.

## More

- Threat model, plugin sandbox and published advisories: https://docs.termix.site/security
- Verify a download: https://docs.termix.site/install/verify
- Signing keys: https://docs.termix.site/install/signing-keys
