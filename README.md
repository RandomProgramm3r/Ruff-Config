# Python Linters Configuration

This repository contains a set of configurations for linters and formatters that I use  in my Python projects. It includes configurations for **flake8** (with a range of plugins), **Black**, and **isort**. These linters helps ensure a consistent code style and improve code quality across projects.

## Repository Structure

- **requirements/flake8-plugins.txt**  
  List of dependencies for flake8 plugins:
  - flake8-absolute-import==1.0.0.2
  - flake8-bugbear==24.8.19
  - flake8-clean-block==0.1.2
  - flake8-commas==4.0.0
  - flake8-eradicate==1.5.0
  - flake8-expression-complexity==0.0.11
  - flake8-implicit-str-concat==0.5.0
  - flake8-print==5.0.0
  - flake8-quotes==3.4.0
  - flake8-return==1.2.0
  - flake8-use-pathlib==0.3.0
  - pep8-naming==0.14.1

- **requirements/linters**  
  Dependency file for the main tools:
  - black==24.8.0
  - flake8==7.1.1
  - isort==5.13.2

- **.flake8**  
  flake8 configuration:
  - Maximum line length: 79 characters
  - Import order style: google
  - Excluded directories: `*/migrations/`, `venv/`, `.git`, `__pycache__`
  - Complexity limits: `max-complexity = 10`, `max-expression-complexity = 7`
  - The flake8-quotes plugin is set to use single quotes

- **.isort.cfg**  
  Configuration for sorting imports with the Black profile:
  - Excluded directories: `migrations`, `venv/`
  - Line length: 79 characters
  - Enforce sorting within sections

- **pyproject.toml**  
  Configuration for Black:
  - Maximum line length: 79 characters
  - String normalization disabled
  - Target Python version: py313
  - Excluded directory: `.venv`

- **.gitignore**  
  A comprehensive .gitignore file для Python.

## Installation

###  Step 1: Clone the Repository

Clone the project repository using Git:

```bash
git clone https://github.com/RandomProgramm3r/Python-Linters-Configuration
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

Install the dependencies (they include all **flake8** dependencies)

```bash
pip install -r requirements/linters.txt
```
