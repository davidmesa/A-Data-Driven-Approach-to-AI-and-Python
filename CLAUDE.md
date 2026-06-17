# CLAUDE.md

Guidance for AI agents (Claude / Cursor) working in this repository.

## What this project is

This is a **Udacity PCEP** (Certified Entry-Level Python Programmer) capstone exercise.
The deliverable is a single guided Jupyter notebook:

- `Project/Udacity - PCEP Project.ipynb` — "Transformational AI: Analyzing Ecommerce
  Large Datasets for Machine Learning".

The notebook walks a student through loading two **Amazon Reviews 2023** datasets from
Hugging Face (`McAuley-Lab/Amazon-Reviews-2023`, the `raw_review_Electronics` and
`raw_meta_Electronics` configs), exploring them with `pandas`, cleaning/filtering by
rating and price, exporting to `.csv` and `.parquet`, and visualizing with `seaborn` /
`matplotlib`.

It is an **educational, fill-in-the-blank** notebook, not production code.

## Repository layout

- `Project/Udacity - PCEP Project.ipynb` — the main notebook (the assignment).
- `Project/readme.md` — placeholder, currently empty.
- `README.md` — Udacity README template (not yet filled in).
- `LICENSE.txt` — Udacity license: **CC BY-NC-ND**, educational use only, non-commercial.
- `CODEOWNERS` — owned by `@davidmesa`.
- `requirements.txt` — pinned dependencies (see versions below).
- `.venv/` — local virtual environment (Python 3.9.19). Not committed.

## Environment

The environment is intentionally pinned to match the Udacity workspace. Do **not** bump
these versions unless the user explicitly asks.

- Python **3.9.19** (installed via `pyenv`, lives in `.venv/`)
- `notebook` 7.1.2
- `datasets` 3.0.1
- `pandas` 2.2.3
- `matplotlib` 3.9.2
- `matplotlib-inline` 0.1.6
- `pyarrow` 17.0.0
- `seaborn` 0.13.2

### Common commands

```bash
# Activate the venv
source ".venv/bin/activate"

# Launch Jupyter Notebook
jupyter notebook

# Reinstall pinned deps
.venv/bin/python -m pip install -r requirements.txt
```

In Jupyter, select the kernel **"Python 3.9.19 (Maestria IA)"** (kernel name
`maestria-ia-py39`).

## How to work in the notebook

- The notebook contains `#<---- YOUR CODE GOES HERE ---->` (and a few
  `<---- YOUR CODE GOES HERE ---->`) placeholders. These are the exercises the student
  must complete. Each is preceded by a "STEPS TO COMPLETE" checklist describing exactly
  what is expected.
- **Do not auto-solve every placeholder unless explicitly asked.** This is graded
  coursework; the learning value is in the student writing the code. When asked for help,
  prefer explaining the concept and the relevant PCEP topic (loops, booleans, `try/except`,
  methods, list `.append`, etc.) over dumping the full answer.
- Keep solutions within the PCEP skill level: basic loops, conditionals, boolean
  operators, exception handling, functions/`return`, lists, and simple `pandas`/`seaborn`
  calls. Avoid introducing advanced idioms the course hasn't covered.
- Reflection cells define `Question1`...`Question7` (and `Name`) via `input()`. Leave the
  answers to the user.

## Conventions & constraints

- Datasets are loaded with `streaming=True` and capped at 100 samples via a `for` loop
  with a `break` — this is deliberate (the full dataset is ~22.6 GB). Do not remove the
  sample limit.
- The notebook produces output files in `Project/` when run: `top_products.csv`,
  `top_products.parquet`, and `user_inputs.txt`. These are generated artifacts.
- License is **non-commercial, no-derivatives educational content**. Do not repurpose the
  Udacity material for anything outside personal coursework.
- Filenames here intentionally contain spaces (e.g. `Udacity - PCEP Project.ipynb`, the
  workspace path `0. Python`). Always quote paths in shell commands.
