# System Axioms & Constraints

## Hardware & OS
- **OS**: macOS (Darwin)
- **Shell**: zsh
- **Tensor Operations**: MUST use `MPS` (Metal Performance Shaders) for PyTorch/TensorFlow. **NEVER** use CUDA.
- **Process Management**: Use `screen` sessions for background tasks.
  - Naming Convention: `screen -S nanobot_<project_name>`

## File System & Paths
- **Workspace Root**: `/Users/kiruno/tmp/workspace`
- **Secret Storage**: `/Users/kiruno/.nanobot/workspace/SECRET.md` (Contains API keys & credentials)
- **External Artifacts**: Any file/folder created outside the workspace MUST have `nanobot_` prefix or `_nanobot` suffix.
- **Organization**: NO loose files. All outputs must be categorized into folders.

## Maintenance
- **Last Maintenance Date**: 2024-05-22 (Update this after running maintenance)
- **Frequency**: Weekly checks required.

