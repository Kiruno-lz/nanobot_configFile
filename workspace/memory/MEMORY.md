# Updated Long‑term Memory

## ClawChat‑Heartbeat
- Project root: `/Users/kiruno/tmp/workspace/clawdchat-heartbeat`
- Contains `heartbeat.py`, `clawdchat‑heartbeat.plist.nanobot`, `HEARTBEAT_SETUP.md`
- LaunchAgent configured to run `/Users/kiruno/miniconda3/envs/nanobot-heartbeat/bin/python` with proper PATH and PYTHONPATH.
- Log written to `~/.nanobot/heartbeat.log`.  Heartbeat script now includes exponential retry logic.

## sol_usdt_liveline
- New project layout:
  - `src/backend/` – FastAPI server
  - `src/frontend/` – static front‑end
  - `config/config.yaml.example` – YAML config template
  - `scripts/` – `run.sh`, `restart.sh`, `test.sh`
  - `Dockerfile` – multi‑stage build for Apple‑Silicon
  - `docker‑compose.yml` – single‑command deployment
  - `README.md` – extended with Docker, CI, and usage sections
  - `.github/workflows/ci.yml` – GitHub Actions for lint, type‑check, tests, and image build
- All tests run successfully with `./scripts/test.sh`.

## MoChat Skill Registration
- Skill definition read from `https://raw.githubusercontent.com/HKUDS/MoChat/.../skill.md`.
- User wants to register as `kirunoBot`.
- Self‑registration attempted via `POST https://mochat.io/api/selfRegister` returned 404; service not found.
- Proposed steps:
  - Verify correct endpoint; may need `/api/v1/selfRegister` or similar.
  - If available, send JSON `{"name":"kirunoBot"}`.
  - Store resulting `clawToken` and `agentUserId` in `~/.nanobot/config.json` under `channels.mochat`.
  - Bind owner via `POST https://mochat.io/api/claw/agents/bind` with email.
  - Send DM with `POST https://mochat.io/api/claw/messages`.

## General Notes
- All projects follow the ‘system engineering’ guideline: keep files in dedicated project subfolders, perform operations atomically, and document changes.
- The assistant will now focus on resolving the MoChat registration error, possibly by querying the MoChat API documentation or using a local mock.

