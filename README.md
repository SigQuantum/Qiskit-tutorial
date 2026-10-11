# Qiskit Tutorial

This notebook uses Python 3.12 in a uv-managed `.venv`, with Qiskit,
JupyterLab, and ipykernel.

## Setup and launch

Run these commands from this directory:

```sh
uv sync --locked
uv run python -m ipykernel install --sys-prefix --name qiskit-tutorial --display-name "Qiskit Tutorial (uv)"
uv run jupyter lab QiskitTutorialWorkshop.ipynb
```

Select **Qiskit Tutorial (uv)** as the notebook kernel. In VS Code, use
**Select Kernel → Python Environments** and choose `.venv/bin/python`.
uv manages the environment; ipykernel runs the notebook's Python code.

If VS Code says `cpython-3.12.12-macos-aarch64-none` needs ipykernel,
it has selected the base interpreter. Open this directory as the VS Code
workspace, then click the kernel name at the top right of the notebook:
**Select Another Kernel → Python Environments → .venv (Python 3.12.12)**.
If `.venv` is missing, run **Python: Select Interpreter** from the Command
Palette and choose **Enter interpreter path**, then select this directory's
`.venv/bin/python`. Return to the notebook and select that environment as
its kernel. Run **Developer: Reload Window** if the list remains stale.
The workspace default points to `.venv`, but an existing notebook kernel
selection must be changed in VS Code.

Skip the notebook's `!pip install` cell in this environment; `uv sync` already
installs the dependencies. IBM account setup requires your own credentials;
skip those cells when using local simulators. Later workshop exercises require
you to fill in code.

To check the selected kernel, run this in a notebook cell:

```python
import sys
print(sys.executable)
```

The path should end in this project's `.venv/bin/python`.
