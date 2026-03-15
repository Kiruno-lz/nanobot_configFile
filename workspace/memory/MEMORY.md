# Updated Long‑term Memory (2026-03-11 18:40)

## Project Status Summary
**Current Date**: 2026-03-11 Wednesday, CST
**Note**: Previous project paths in MEMORY.md were incorrect. Projects not found at recorded locations.

### 1. nanobot Core Infrastructure
- **Working Directory**: `/Users/kiruno/.nanobot/workspace`
- **Memory Files**:
  - Long-term: `memory/MEMORY.md`
  - History Log: `memory/HISTORY.md` (grep-searchable)
- **Skills**: Located in `skills/` subfolder
  - Available skills: clawchat, git-essentials, self-improving-agent

### 2. Archived Projects (Deleted by User)
#### ClawChat‑Heartbeat (Status: Deleted)
- **Last Known Path**: `/Users/kiruno/tmp/workspace/clawdchat-heartbeat`
- **Deletion Date**: 2026-03-11
- **Components**:
  - `heartbeat.py` – Heartbeat script with exponential retry logic
  - `clawdchat‑heartbeat.plist.nanobot` (LaunchAgent)
  - `HEARTBEAT_SETUP.md` – Setup documentation
  - Log: `~/.nanobot/heartbeat.log`

#### sol_usdt_liveline (Status: Deleted)
- **Last Known Path**: `/Users/kiruno/tmp/workspace/sol_usdt_liveline`
- **Deletion Date**: 2026-03-11
- **Components**:
  - `src/backend/` – FastAPI server
  - `src/frontend/` – static front‑end
  - `config/config.yaml.example`
  - `scripts/run.sh`, `restart.sh`, `test.sh`
  - `Dockerfile` (Apple‑Silicon optimized)
  - `docker-compose.yml`
  - `.github/workflows/ci.yml`

#### MoChat Skill Registration (Status: Blocked)
- **Target**: Register as `kirunoBot`
- **Issue**: 404 error on `POST https://mochat.io/api/selfRegister`
- **Next Steps**:
  - Verify correct endpoint (`/api/v1/selfRegister`?)
  - Store credentials in `~/.nanobot/config.json` under `channels.mochat`
  - Bind owner via email

### 3. General Notes
- All projects follow the 'system engineering' guideline: keep files in dedicated project subfolders, perform operations atomically, and document changes.
- **Action Item**: Projects need to be re-discovered or recreated at their correct locations.
