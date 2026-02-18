# Agent Standard Operating Procedures (SOP)

## Phase 0: Self-Correction & Maintenance (The Gardener Protocol)
*Trigger: At the start of a session, check `MEMORY.md` for `Last Maintenance Date`.*
- If > 7 days since last check:
  1.  **Archive**: Move loose files to `archive/` or project folders.
  2.  **Prune & Merge**: Scan `ENVIRONMENTS.md`. Identify similar Conda environments, merge them into a shared env, and update project refs.
  3.  **Update**: Update `ENVIRONMENTS.md` and `MEMORY.md`.

## Phase 1: Anchoring (Project Initialization)
1.  **Read/Create Manifests**:
    - `PROJECT_STATUS.md`: High-level goals, current phase (User-facing).
    - `NANOBOT_TASK.md`: Granular execution steps, logs, debug info (Agent-facing).
2.  **Version Control Setup**:
    - Check for `.git` directory. If not present, run `git init`.
    - Create a `.gitignore` file with sensible defaults for the project type (e.g., Python, Node.js).
3.  **Credentials**:
    - **Read `SECRET.md`**: Load necessary API keys/tokens from `/Users/kiruno/.nanobot/workspace/SECRET.md`.
    - **Security**: NEVER print keys to logs or commit them to code. Inject as environment variables.
4.  **Environment Strategy**:
    - Check `ENVIRONMENTS.md`. Can an existing environment be reused?
    - If yes -> Reuse and update entry.
    - If no -> Create new Conda env `nanobot_env_<name>`, install deps, and register in `ENVIRONMENTS.md`.

## Phase 2: Test-Driven Execution (TDD)
1.  **Design**: Plan the architecture. Aim for high concurrency (Backend) or responsive beauty (Frontend).
2.  **Test First**: Write Unit Tests and Integration Tests *before* complex logic.
3.  **Implement**: Write code to pass tests.
4.  **Runtime Verification**:
    - Execute the code in the actual environment.
    - **Self-Correction**: If it fails, read logs, hypothesis, fix, retry. (Do not ask user unless blocked 3x).
5.  **Refactor**:
    - Consolidate logic.
    - Add comments and docstrings.
    - Ensure code is "Masterpiece" quality.
6.  **Commit Changes**:
    - After a logical unit of work is stable (e.g., a feature is complete, a bug is fixed), stage and commit changes.
    - **Commit Message Standard**: MUST follow the **Conventional Commits** specification.
      - Format: `<type>[optional scope]: <description>`
      - Examples:
        - `feat: Add user login endpoint`
        - `fix: Correct calculation error in payment module`
        - `refactor: Simplify database connection logic`
        - `test: Add unit tests for user model`
        - `docs: Update API documentation for /users`

## Phase 3: Delivery & Deployment
1.  **Deployment**:
    - Use `screen -S nanobot_<project_name>` for background execution.
    - Verify service health (Health Check).
2.  **Final Commit & Tagging**:
    - Make a final commit for any deployment-related changes.
    - Create a git tag for the release (e.g., `git tag -a v1.0.0 -m "Initial release"`).
3.  **Documentation**:
    - Update `PROJECT_STATUS.md` with "Completed".
    - Update `ENVIRONMENTS.md` if deps changed.
