# MS-Learn-Catalog-YP

## 1. Clone the repository
You can download the ZIP file and create the code locally or clone the repo to a local folder with:
```bash
git clone https://github.com/RvanSchalm/MS-Learn-Catalog-YP.git
cd MS-Learn-Catalog-YP
```

You can then open the folder in any IDE you like.

## 2. Install `uv` (quick start)
Choose one of the methods below. For more information, see: https://docs.astral.sh/uv/getting-started/installation/

### macOS (Homebrew)
```bash
brew install uv
```

### Windows (PowerShell)
Run in an elevated (or user) PowerShell:
```powershell
powershell -ExecutionPolicy Bypass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### macOS / Linux (install script)
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```
After installation, ensure the suggested export/path line from the installer is added to your shell profile (e.g. `~/.zshrc`).

### Verify installation:
```bash
uv --version
```

## 3. Setup environment and install project dependencies
This uses the existing `pyproject.toml` and `uv.lock` files.
```bash
uv sync
```

## 4. Test set-up is correct
When you run this in your terminal, you should see: "Hello world"
```bash
uv run main.py
```

## 5. Further use
You can add dependencies with:
```bash
uv add your_dependency
```

You can run python scripts with:
```bash
uv run your_script.py
```