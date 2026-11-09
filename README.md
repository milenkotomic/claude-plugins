# claude-plugins

My Claude Code plugins, as one marketplace. Each plugin lives in its own
repo; this repo is only the catalog.

| Plugin | What it does |
|---|---|
| [review-map](https://github.com/milenkotomic/review-map) | Turn a diff, branch, PR or working tree into a reviewer-oriented map of the change, rendered as a styled HTML page. |
| [handoff](https://github.com/milenkotomic/handoff) | Save the live state of a task outside the repo and resume it in a fresh session. |

## Install

```sh
claude plugin marketplace add milenkotomic/claude-plugins
claude plugin install review-map@milenkotomic
claude plugin install handoff@milenkotomic
```

Inside Claude Code: `/plugin marketplace add milenkotomic/claude-plugins`,
then `/plugin install <name>@milenkotomic`. Start a new session afterwards.

## Update

```sh
claude plugin marketplace update milenkotomic
claude plugin update <name>@milenkotomic
```

Plugins install from each repo's default branch, so a push there reaches
you on the next update.

## Add a plugin

Add an entry to `.claude-plugin/marketplace.json` with
`"source": { "source": "github", "repo": "milenkotomic/<repo>" }`, then run
`claude plugin validate .` and push.

## License

MIT, see [LICENSE](LICENSE). Each plugin carries its own license.
