## Notebook Run Instructions

Quick steps to run the core notebooks in this workspace locally.

Prerequisites
- Python 3.8+ (tested with 3.13)
- `pip` available

Setup (recommended)
1. Create and activate a virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install dependencies:

```powershell
pip install -r requirements.txt
```

3. (Optional) Register the kernel used when executing notebooks programmatically:

```powershell
python -m ipykernel install --user --name python3 --display-name python3
```

Run notebooks (examples)

```powershell
jupyter nbconvert --to notebook --execute "level2_wine_quality.ipynb" --output executed_level2_wine_quality.ipynb --ExecutePreprocessor.timeout=600
jupyter nbconvert --to notebook --execute "level2_fraud_detection.ipynb" --output executed_level2_fraud_detection.ipynb --ExecutePreprocessor.timeout=600
```

Or open the folder in JupyterLab/Notebook and "Run All" interactively:

```powershell
jupyter lab
```

Notes
- The notebooks have been made resilient to missing CSV files by creating small synthetic fallback datasets where appropriate, so they can run end-to-end even if original data files are absent.
- Executed outputs are written with the `executed_` prefix when using the `nbconvert --execute` command above.
