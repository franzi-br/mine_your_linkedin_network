# LinkedIn Network Kit for Claude

Turn your LinkedIn data export into a ranked list of the people most likely to help you land your next role, each with a reason and a ready to send opening line, plus a tracker and an outreach playbook to work the list.

Built and tested in a live senior job search in Berlin, October 2026.

## What you get

In about an hour, Claude reads your full LinkedIn export and returns:

1. **Ranked matches**: decision makers, referral sources, intermediaries, investors and warm contacts, scored 1 to 5 against your target role, with the signals used and why each person fits.
2. **Opening lines** in one or two languages, written as an ask for advice, never for a job.
3. **A gap check**: which kinds of contact your network is missing, and which target companies you have no one at.
4. **An outreach tracker** set up from the start, so you can see your reply rate and what converts.

## Quick start

1. Request your full LinkedIn archive (Settings & Privacy, Data privacy, Get a copy of your data). It can take up to a day.
2. Answer the eight questions in [docs/setup.md](docs/setup.md).
3. Fill in [prompt/prompt.md](prompt/prompt.md) with your answers.
4. Run it in Claude with the zip attached. When the shortlist is back, add what only you know about the people on it, then work the list with the [outreach playbook](docs/outreach_playbook.md).

Works best in a Claude Project with your CV uploaded. For a Google Sheet as output, connect Google Drive and Google Sheets first.

## What's in this repo

| Path | What it is |
| --- | --- |
| [prompt/prompt.md](prompt/prompt.md) | The prompt, plus the second pass for personal context |
| [docs/setup.md](docs/setup.md) | Export steps, the eight questions, how to run it, limits |
| [docs/outreach_playbook.md](docs/outreach_playbook.md) | How to reach out, what to write, follow up cadence |
| [examples/filled_prompt_example.md](examples/filled_prompt_example.md) | A filled prompt for a fictional user |
| [templates/outreach_tracker.csv](templates/outreach_tracker.csv) | Tracker columns, if you'd rather keep it yourself |

## Privacy

Your export contains other people's names and some email addresses. Keep it private, don't share the output publicly, and delete the zip when you're done. This repo's `.gitignore` blocks zip and CSV files so a fork can't commit an export by accident. Nothing in this kit sends messages for you: every message is reviewed and sent by you.

## Limits

Claude only sees what is in the export: no About sections, posts, mutual connections or messages. Company size, stage and location come from Claude's general knowledge and are marked "(inferred)". Titles can be years out of date. Treat the list as a strong first draft, not a verdict.

## Credits

A few outreach practices build on ideas from Laszlo Bock's *Apply Within* job search series (2026), shared by the author on LinkedIn. They are marked "(after Bock)" in the playbook and written in our own words; read his original for his full guidance. Everything else comes from using this kit.

Created by Franziska Bruno Rivera.

## Contributing and license

Improvements and results from your own runs are welcome; see [CONTRIBUTING.md](CONTRIBUTING.md). Released under the [MIT License](LICENSE).
