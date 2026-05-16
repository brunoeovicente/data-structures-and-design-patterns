# Data Structures and Design Patterns

Personal repository created to study:

* Algorithms
* Data Structures
* OOP
* Design Patterns
* Concurrency
* Computer Science fundamentals

Language:

* Python

---

# Project Structure

```text
C:\dev\studies\data-structures-and-design-patterns
│
├── algorithms/
├── data-structures/
├── oop/
├── design-patterns/
├── concurrency/
├── notes/
├── tests/
│
├── .gitignore
├── README.md
├── pyproject.toml
└── poetry.lock
```

---

# Creating the Repository

Recommended flow:

1. Create the repository on GitHub
2. Clone it into `C:\dev\studies`

Example:

```powershell
cd C:\dev\studies

git clone https://github.com/YOUR_USER/data-structures-and-design-patterns.git
```

---

# Poetry Setup

This project uses Poetry for:

* Virtual environments
* Dependency management
* Development tooling

Tool:

* Poetry

---

# Installing Poetry

Recommended installation using `pipx`:

```powershell
pip install pipx
pipx install poetry
```

Check installation:

```powershell
poetry --version
```

---

# Configure Poetry Virtual Environment

Recommended configuration:

```powershell
poetry config virtualenvs.in-project true
```

This creates the virtual environment inside:

```text
.venv/
```

instead of using a global hidden location.

---

# Initialize Poetry

Inside the repository:

```powershell
poetry init
```

---

# pyproject.toml

Recommended configuration:

```toml
[project]
name = "data-structures-and-design-patterns"
version = "0.1.0"
description = ""
authors = [
    { name = "Bruno Vicente", email = "brunoeovicente@gmail.com" }
]
readme = "README.md"
requires-python = ">=3.12"

[tool.poetry]
package-mode = false

[build-system]
requires = ["poetry-core>=2.0.0,<3.0.0"]
build-backend = "poetry.core.masonry.api"
```

---

# Why `package-mode = false`

This repository is primarily:

* a study repository
* a playground
* an algorithms repository
* not a distributable Python package

So Poetry should be used only for:

* dependency management
* virtual environments
* tooling

---

# Install Dependencies

Generate lock file:

```powershell
poetry lock
```

Install environment:

```powershell
poetry install
```

Activate shell:

```powershell
poetry shell
```

---

# Recommended Development Dependencies

```powershell
poetry add pytest black ruff mypy ipykernel --group dev
```

Installed tools:

| Tool      | Purpose         |
| --------- | --------------- |
| pytest    | Testing         |
| black     | Formatter       |
| ruff      | Linter          |
| mypy      | Type checking   |
| ipykernel | Jupyter support |

---

# Running Python Files

Example:

```powershell
poetry run python algorithms/sorting/bubble_sort.py
```

Running tests:

```powershell
poetry run pytest
```

---

# .gitignore

Recommended `.gitignore`:

```gitignore
# Virtual environment
.venv/

# Python cache
__pycache__/
*.py[cod]

# Distribution / packaging
dist/
build/
*.egg-info/

# Pytest
.pytest_cache/

# Mypy
.mypy_cache/

# Ruff
.ruff_cache/

# Jupyter
.ipynb_checkpoints/

# IDEs
.idea/
.vscode/

# OS
.DS_Store
Thumbs.db
```

---

# Git Workflow

## Check repository status

```powershell
git status
```

---

## Check unstaged changes

```powershell
git diff
```

Specific file:

```powershell
git diff pyproject.toml
```

---

## Stage files

Recommended:

```powershell
git add pyproject.toml
git add poetry.lock
git add .gitignore
```

---

## Check staged changes

```powershell
git diff --staged
```

or:

```powershell
git diff --cached
```

---

## Commit changes

```powershell
git commit -m "Initialize Poetry environment"
```

---

## Push to GitHub

```powershell
git push origin main
```

---

# Notes

The `notes/` folder can be used for:

* Markdown notes
* Complexity analysis
* Design pattern explanations
* Personal observations
* Benchmarks
* Theoretical summaries

Example:

```text
notes/
    big-o.md
    linked-list.md
    observer-pattern.md
```

---
