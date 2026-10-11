# Qiskit Tutorial

Install Git and uv, then run:

```sh
git clone https://github.com/SigQuantum/Qiskit-tutorial.git
cd Qiskit-tutorial
uv sync --locked
uv run python -m ipykernel install --user --name qiskit-tutorial --display-name "Qiskit Tutorial (uv)"
```

Open the notebook in JupyterLab:

```sh
uv run jupyter lab QiskitTutorialWorkshop.ipynb
```

Select **Qiskit Tutorial (uv)** as the kernel.

For VS Code, install the **Python** and **Jupyter** extensions, open the
repository folder, and open `QiskitTutorialWorkshop.ipynb`. In the notebook's
kernel selector, choose **Select Another Kernel → Python Environments → .venv**.

Skip the notebook's `!pip install` cell; dependencies are already installed.
IBM account cells require your own credentials and can be skipped for local simulation.
