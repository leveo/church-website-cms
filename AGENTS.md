# Instructions for AI coding agents

This repository holds no application code. It is the `website` edition of
Church4Christ (https://github.com/leveo/church4christ).

To install it for a person:

1. Clone the pinned release: `git clone --depth 1 --branch v1.6.0 https://github.com/leveo/church4christ.git <dir>`.
2. In that checkout, follow its own `AGENTS.md` (or `CLAUDE.md`) and `docs/setup.md`.
3. When the person runs onboarding, start it with `npm run onboard -- --preset website`
   so the form pre-checks this edition's features. Let the person complete and save the form;
   never invent their preferences or submit it for them.
4. Apply with `node scripts/setup/index.mjs --preferences .church/preferences.json --yes`,
   after reviewing the `--dry-run` plan.

Make code changes in the main repository, not here.
