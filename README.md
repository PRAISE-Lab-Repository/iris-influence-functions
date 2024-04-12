# Iris Dataset Influence Functions Explorations

![A stylzed photograph of the influence function theorem in front of a background of irises](./repository-logo.jpg)

This repository contains jupyter notebooks which apply Koh et Liang's 2017 paper on influence functions on the toy `scikit-learn` Iris dataset. It uses a fork of Nimar B.'s Pytorch implementation of Koh et Liang's methods maintained by the team at PRAISE Labs ([link here](https://github.com/PRAISE-Lab-Repository/pytorch_influence_functions)). The purpose of this repository is to benchmark and validate the use of influence functions for interpretability on small to medium-sized models, and ultimately serve as an exploratory effort towards using influence functions for real-world applications.

# Setup

This repository using Python virtual environments for dependency management, and fast.ai's [nbdev](https://nbdev.fast.ai/tutorials/git_friendly_jupyter.html) pre-commit hooks for version-controlling Jupyter notebooks.

## Quickstart
In order to run this repository, clone it and create a Python virtual environment:

```bash
python -m venv .venv
```

Activate the virtual environment and install dependencies from the provided `requirements.txt` file:

```bash
source .venv/bin/activate
python -m pip install -r requirements.txt
```

This notebook depends upon PRAISE Lab's fork of the [nimarb/pytorch_influence_functions](https://github.com/nimarb/pytorch_influence_functions) repository, which contains various fixes. Hence the version of `pytorch-influence-functions` available on pip will *not* work by default. Instead, clone and install the PRAISE Labs fork from GitHub:

```bash
git clone https://github.com/PRAISE-Lab-Repository/pytorch_influence_functions.git
cd pytorch_influence_functions/
python setup.py install
``` 

In order to keep version control tidy, we use fast.ai's [nbdev pre-commit hooks](https://nbdev.fast.ai/tutorials/pre_commit.html). In order to set this up, run:

```bash
pre-commit install
```

Now you are able to begin working on the Jupyter notebooks within this repository.

# Notebooks

Right now, this repository only contains the `iris_influence.ipynb` notebook, which calculates influence on a simple neural network.