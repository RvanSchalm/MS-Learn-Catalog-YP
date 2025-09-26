# MS Learn Unit URL Extractor

## Project set up
Go to the `README_SETUP.md` file and follow the instructions.

## Project description
### Goal
Provide a simple, reproducible workflow to (1) extract the Microsoft Learn Catalog JSON and (2) extract all unit (lesson) URLs for a given Microsoft Learn course so they can be imported into Google NotebookLM (`https://notebooklm.google.com/`).

### Why
Manually copying unit links is slow. The public Microsoft Learn Catalog API exposes structured metadata you can filter programmatically. Once you have a clean list of unit URLs, you can feed them directly into NotebookLM.

## Two‑Step Process (Conceptual)
1. Fetch the catalog JSON from the Microsoft Learn Catalog API. (`https://learn.microsoft.com/api/catalog/`)
2. Given a human course name (e.g. "Designing and implementing a data science solution on Azure"), locate the matching course object and extract all associated unit (lesson) URLs, then save them in your preferred format.

You should use GitHub Copilot to create a solution for this project. Make sure to put it in Agent mode and select a model of your choice.

## Current Minimal File Layout (You can evolve this)
```
MS-Learn-Catalog-YP/
  .github/               # Here all your Copilot instructions can be stored
  data/                  # Output folder for your data
  .gitignore             # Can be used to stop git from tracking files
  .python-version        # There to instantiate the requried python version
  main.py                # Currently prints "Hello world"
  pyproject.toml         # There to set up the environment for you
  README_SETUP.md        # There to help you set up the repo and environment
  README.md              # (optional) Can be adjusted once you have your solution ready
  uv.lock                # There to set up the environment for you
```

At the moment only `main.py` exists (prints "Hello world"). You are free to extend this with extra files or write all code in there. The data folder can be used, but is not necessary.

## Notes
- Copilot might warn you that the Catalog schema might evolve, but you can tell Copilot to focus on this specific schema and not make it future proof for this exercise (do not start (HTML) scraping the websites!).
- The MS Learn architecture is as follows: `Course -> Learning Path -> Module -> Unit`