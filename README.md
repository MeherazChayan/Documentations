# Technical Documentation Collection

Five project-specific documentation collections, organized as a Sphinx / reStructuredText documentation site.

**Projects:** [NewsProof](docs/projects/newsproof/index.rst) · [My University Portal](docs/projects/university/index.rst) · [MedBot Assist](docs/projects/medbot/index.rst) · [Care Cloud](docs/projects/carecloud/index.rst) · [ReliableVAEP](docs/projects/vaep/index.rst)

The documents describe **publicly documented behavior** from the corresponding upstream repositories. Source references appear on every project page. This documentation repository does not duplicate application code.

## Build locally

Python 3.10+ recommended for the documentation tooling (not necessarily the application projects):

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements-docs.txt
python -m sphinx -b html -W --keep-going docs docs/_build/html
```

Open `docs/_build/html/index.html`. On macOS/Linux use `python3 -m venv .venv` and `source .venv/bin/activate`.

## Scope and verification

These pages were drafted against publicly visible project READMEs and repository directories. The source repositories were **not cloned or executed** in this environment. A documentation site's successful build does not verify application installation, safety, scientific reproducibility, or API responses. Consult [VERIFICATION.md](VERIFICATION.md) before publishing as a personal writing sample.

## Publication

GitHub Actions verifies the HTML build. GitHub Pages hosting can be configured separately. Publishing the repository and finalizing authorship remain the repository owner's responsibility.
