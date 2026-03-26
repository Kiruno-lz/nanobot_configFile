# Conda Environment Registry

## Work Policy
> **⚙️ Python/pip Execution Rule**: All Python and pip commands should use the `default` conda environment by default.

### PATH Configuration
```bash
# This line is automatically added to ~/.zshrc:
export PATH="/opt/miniconda3/envs/default/bin:$PATH"
```
> **Note**: This ensures that `python3` and `pip3` from the `default` environment are found first in the PATH.

| Environment Name | Python Version | Key Libraries | Linked Projects | Last Updated |
| :--- | :--- | :--- | :--- | :--- |
| `default` | 3.13 | sumy, nltk, requests | nanobot core | 2026-03-15 |
| `nanobot` | 3.12 | nanobot framework | nanobot agent | - |
| `example_env` | 3.10 | numpy, pytorch(mps) | project_alpha | 2024-01-01 |

*Note: Before creating a new environment, ALWAYS check this list for potential reuse.*

## Available Environments
```bash
conda env list
# Output:
# base                 * /opt/miniconda3
# default              /opt/miniconda3/envs/default
# nanobot              /opt/miniconda3/envs/nanobot
# 3dprinting           /opt/miniconda3/envs/3dprinting
# flamingo             /opt/miniconda3/envs/flamingo
# memU                 /opt/miniconda3/envs/memU
```

## Switching Between Environments
```bash
# To use a specific environment:
conda activate <env_name>

# Examples:
conda activate nanobot      # For nanobot development
conda activate 3dprinting   # For 3D printing projects
conda activate default      # Default for Python/pip operations
```
