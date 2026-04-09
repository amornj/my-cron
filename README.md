# my-cron

CLI scripts for daily and weekly automated tasks via OpenClaw.

## Scripts

### `daily-cron`

Runs three jobs every morning:

- **Echo: Daily Tweet Summary** — summarizes recent tweets
- **Daily Market Briefing** — market overview
- **Daily Bangkok Weather** — local weather report

### `literature-cron`

Runs the cardiology literature review for the current day of the week, then emails the PDF to Readwise Reader.

| Day | Topic |
|-----|-------|
| Mon | Complex PCI Review |
| Tue | Heart Failure |
| Wed | DM / Lipid / Obesity |
| Thu | Structural Heart |
| Fri | ACS / Shock / MCS / Critical Care |
| Sat | Cardiomyopathy / PH / AF / Pericardial |
| Sun | Aging & Anti-Aging |

After each run, the generated PDF is emailed to `amornj@library.readwise.io` (Readwise Reader email import) via `gog gmail send`.

## Requirements

- [`openclaw`](https://docs.openclaw.ai/cli) — agent runtime and cron scheduler
- [`gog`](https://github.com/gogcli/gog) — Google Workspace CLI (Gmail send)
