# Transformational AI: Analyzing Ecommerce Large Datasets for Machine Learning

A Udacity **PCEP** (Certified Entry-Level Python Programmer) capstone project. This
notebook takes on the role of a data scientist at the fictional company "Transformational
AI", loading two **Amazon Reviews 2023** datasets from Hugging Face, transforming and
analyzing them with `pandas`, visualizing trends with `seaborn` / `matplotlib`, and
exporting cleaned data to `.csv` and `.parquet` for the machine learning team.

The project reinforces core PCEP concepts: variables and data types, boolean operators,
`for` loops, functions and `return`, exception handling (`try`/`except`), lists and the
`.append` method, and method invocation on objects.

## Getting Started

These instructions get a copy of the project running locally in Jupyter Notebook.

### Dependencies

- Python **3.9.19**
- `notebook` 7.1.2
- `datasets` 3.0.1
- `pandas` 2.2.3
- `matplotlib` 3.9.2
- `matplotlib-inline` 0.1.6
- `pyarrow` 17.0.0
- `seaborn` 0.13.2

All Python packages and their pinned versions are listed in [`requirements.txt`](requirements.txt).

### Installation

The project uses an isolated virtual environment pinned to Python 3.9.19 to match the
Udacity workspace.

1. Install Python 3.9.19 (e.g. via [`pyenv`](https://github.com/pyenv/pyenv)):

```bash
pyenv install 3.9.19
```

2. Create and activate a virtual environment in the project root:

```bash
~/.pyenv/versions/3.9.19/bin/python -m venv .venv
source ".venv/bin/activate"
```

3. Install the pinned dependencies:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

4. (Optional) Register a Jupyter kernel for this environment:

```bash
python -m ipykernel install --user --name maestria-ia-py39 --display-name "Python 3.9.19 (Maestria IA)"
```

5. Launch Jupyter Notebook and open the project:

```bash
jupyter notebook
```

Then open `Project/Udacity - PCEP Project.ipynb` and select the
**"Python 3.9.19 (Maestria IA)"** kernel.

## Project Instructions

Work through `Project/Udacity - PCEP Project.ipynb` from top to bottom. The notebook is a
guided, fill-in-the-blank assignment:

- Complete each `#<---- YOUR CODE GOES HERE ---->` placeholder, following the
  "STEPS TO COMPLETE" checklist that precedes it.
- Answer the reflection prompts (`Question1` through `Question7`) in the input cells.
- Add your name in the final section.

The notebook is organized into six parts:

1. **Preparing the Environment** — verify Python / Jupyter versions and install packages.
2. **Download the Reviews Dataset** — stream the first 100 `raw_review_Electronics`
   samples into a `pandas` DataFrame and inspect it.
3. **Download the Reviews Metadata Dataset** — stream `raw_meta_Electronics` and build a
   robust product lookup with exception handling.
4. **Comparing the Datasets** — explore columns, data types, and summaries
   (`.columns`, `.dtypes`, `.info()`).
5. **Preparing the Data for the ML Team** — filter top products by rating and price,
   compute percentages, and export to `.csv` and `.parquet`.
6. **Visualizing the Data** — build histograms, scatterplots, and a combined dashboard.

> Note: the source datasets are large (~22.6 GB), so the notebook intentionally uses
> `streaming=True` and caps collection at 100 samples per dataset.

### Deliverables

After running the notebook you should have, in the `Project/` folder:

- The completed notebook with cell outputs included
- `user_inputs.txt` — your answers to all reflection questions
- `top_products.csv` — the cleaned top-products dataset
- `top_products.parquet` — the same dataset in Parquet format

## Built With

- [Python](https://www.python.org/) - Programming language (3.9.19)
- [Jupyter Notebook](https://jupyter.org/) - Interactive computing environment
- [Hugging Face `datasets`](https://huggingface.co/docs/datasets) - Dataset access and streaming
- [pandas](https://pandas.pydata.org/) - Data manipulation and analysis
- [seaborn](https://seaborn.pydata.org/) & [matplotlib](https://matplotlib.org/) - Data visualization
- [PyArrow](https://arrow.apache.org/docs/python/) - Reading/writing Parquet files

Dataset: [Amazon Reviews 2023 (`McAuley-Lab/Amazon-Reviews-2023`)](https://huggingface.co/datasets/McAuley-Lab/Amazon-Reviews-2023).

## License

[License](LICENSE.txt) — Udacity educational content (CC BY-NC-ND, non-commercial use only).
