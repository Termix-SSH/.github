# Governance

Termix is run by a small team. This file says who decides what, who does which job, and how the project keeps going if someone is away. It covers every repo in the [Termix-SSH](https://github.com/Termix-SSH) organization.

## Roles

| Role            | Who                                                                                | What they do                                                                                                                                                                                                         |
| --------------- | ---------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Lead maintainer | [LukeGus](https://github.com/LukeGus) (Luke Gustafson)                             | Sets direction, has the final say, reviews and merges changes, cuts releases, handles security reports, holds the offline root signing keys.                                                                         |
| Maintainers     | [ZacharyZcR](https://github.com/ZacharyZcR), [Xenthys](https://github.com/Xenthys) | Review and merge pull requests, triage issues and security reports, approve release runs (the `release` environment). ZacharyZcR is admin on the main repos and takes over releases and signing if the lead is away. |
| Contributors    | Anyone                                                                             | Open issues and pull requests, write plugins, translate, help others on Discord.                                                                                                                                     |
| Bots            | Termix CI (GitHub App), Dependabot, the Triage Bot                                 | Push release commits, keep dependencies current, label and review. They act only through workflows the maintainers control.                                                                                          |

Tasks the roles must do:

- Answer security reports within the times in [SECURITY.md](SECURITY.md).
- Make sure every change to `main` or a `dev-*` branch goes through a pull request with checks, or is a signed commit by the lead.
- Approve each release run before it signs anything.
- Follow and enforce the [Code of Conduct](CODE_OF_CONDUCT.md).

## How decisions are made

Most decisions happen in the open, in issues and pull requests. A maintainer can merge a change once its checks pass. When people disagree, the lead maintainer makes the call and says why.

Bigger changes get a public issue first: breaking the plugin API, adding or removing an official plugin, changing the security policy or the signing keys. Plans for the next year are on the [roadmap](https://docs.termix.site/roadmap).

## If someone is away

The project must keep going if any one person can't continue.

- Maintainers can create and close issues and review and merge changes in every repo.
- ZacharyZcR is admin on the core, registry, docs, mobile and CLI repos and approves release runs, so they can cut releases if the lead maintainer is gone. The lead maintainer has arranged private access for ZacharyZcR to one of the offline root signing keys, so plugin and release signing can continue.
- The domains, the GitHub organization and the app store accounts are covered by the same private arrangement.

If the lead maintainer stops answering for 30 days, the maintainers decide together who leads.

## Becoming a maintainer

Contributors who have made good changes and reviews over a few months can be invited by the lead maintainer, after talking with the other maintainers. Maintainers who step back keep their credit and lose their access.

## Changing this file

Changes to this file go through a pull request and need the lead maintainer's approval.
