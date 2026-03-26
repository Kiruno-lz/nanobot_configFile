# Long‑term Memory (Updated as of 2026-03-15)

## Project Status Summary
- **ClawChat‑Heartbeat** – Deleted on 2026-03-11. Last known path `/Users/kiruno/tmp/workspace/clawdchat-heartbeat`.
- **sol_usdt_liveline** – Deleted on 2026-03-11. Last known path `/Users/kiruno/tmp/workspace/sol_usdt_liveline`.
- **MeloSeed** – Next‑js project located at `~/Documents/_code/vibe/MeloSeed`. Successfully started (`npm run dev`) on port 3001. Generated music via "Germinate Seed" button; generation in progress.

## Environment & Tooling
- **Conda Environments**: `default` (Python 3.13, contains sumy, nltk, tmux), `nanobot`, `nanobot-heartbeat`, `3dprinting`, `flamingo`, `memU`.
- **Work Policy** (added to `ENVIRONMENTS.md` and `.zshrc`):
  - Shell auto‑activates `default` conda environment on startup.
  - PATH prepended with `/opt/miniconda3/envs/default/bin` so `python`, `python3`, `pip`, `pip3` resolve to the `default` env.
  - Users may switch environments via `conda activate <env>`.
- **.zshrc changes**: added auto‑activate block and PATH export.

## Installed CLI Tools
- **tmux** – Homebrew installed, version 3.6a.
- **sumy** – Python package installed (v0.12.0) for summarization.
- **nltk** – Python package installed (v3.9.3).
- **summarize skill** – now functional.
- **pyautogui** – installed for screenshot capability.
- **pillow** – installed for image handling.

## Skills & Tools Availability
- **Tools**: `read_file`, `write_file`, `edit_file`, `list_dir`, `exec`, `web_search`, `web_fetch`, `message`, `spawn`, `cron`, `browser_action`.
- **Skills**: `clawchat`, `git-essentials`, `self-improving-agent`, `summarize`, `tmux` (now usable).

## Browser Action Activities


## Files Updated
- `~/.nanobot/workspace/memory/MEMORY.md` – marked projects as deleted, added MeloSeed entry.
- `~/.nanobot/workspace/ENVIRONMENTS.md` – added work policy section.
- `~/.zshrc` – added conda activation and PATH export.

## Notes
- All future Python/pip commands will default to the `default` conda environment.
- Screenshot of Bilibili video was successfully saved after converting RGBA to RGB.
