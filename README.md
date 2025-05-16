# Ruff Config

[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)

This repository provides pre-configured configurations of **Ruff**, a fast tool for linting and formatting Python code. The ready-made **ruff.toml** file makes it easy to implement uniform standards of style and code quality in your projects.

## Installation

###  Step 1: Clone the Repository

Clone the project repository using Git:

```bash
git clone https://github.com/RandomProgramm3r/Ruff-Config
```

###  Step 2: Create and activate a virtual environment

Create a virtual environment using the `venv` command, which allows you to isolate project dependencies:

```bash
python3 -m venv venv #  Linux/MacOS
python -m venv venv # Windows
```

Activate the virtual environment:

```bash
source venv/bin/activate #  Linux/MacOS
source venv/Scripts/activate # Windows
```

###  Step 3: Installing Dependencies

```bash
pip install -r requirements.txt
```

## Using Ruff

To integrate Ruff into your workflow, use the following commands:

```bash
# Run linting checks on all files
ruff check .

# Automatically fix all fixable lint issues
ruff check . --fix

# Format code according to Ruff’s rules
ruff format .
```

## CI with GitHub Actions

This repository includes a GitHub Actions workflow (`.github/workflows/ruff.yml`) that on every push or pull request to `main` will:

- Check out the code
- Set up Python 3.13
- Run Ruff via the official action
- Verify formatting with `ruff format --check`

To customize, edit `.github/workflows/ruff.yml` or adjust your `ruff.toml`.