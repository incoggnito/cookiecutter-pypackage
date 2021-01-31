# Cookiecutter PyPackage

[Cookiecutter](https://github.com/cookiecutter/cookiecutter) template for Python package.

## Features

- `src` project structure - [how and why](https://bskinn.github.io/My-How-Why-Pyproject-Src)
- Checks & tests with [tox](https://tox.readthedocs.io)
  - Formatting with [black](https://github.com/psf/black)
  - Check sorted imports with [isort](https://pycqa.github.io/isort/)
  - Code analysis with [pylint](https://www.pylint.org)
  - Type checks with [mypy](http://mypy-lang.org)
  - Testing with [pytest](https://pytest.org)
- `pyproject.toml` for configuration
- CI and deployment to PyPI with [GitHub Actions](https://github.com/features/actions)
- Documentation with [Sphinx](https://www.sphinx-doc.org)
  - Easy API documentation with [autosummary](https://www.sphinx-doc.org/en/master/usage/extensions/autosummary.html)
  - Leverage type annotations for docs with [sphinx-autodoc-typehints](https://github.com/agronholm/sphinx-autodoc-typehints)
- Changelog based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)

## Quickstart

Install the latest Cookiecutter if you haven't installed it yet (this requires Cookiecutter 1.4.0 or higher):

- `pipx` to install the global packages (check with witch)

  ```sh
  # pipx for global package or use `sps python-*` in Arch
  python3 -m pip install --user pipx
  python3 -m pipx ensurepath
  pipx install cookiecutter, jupyter, black, flake8, mypy, tox, ipykernel, iypthon, isort, poetry
  ```

- `cookiecutter` to load the template and fill the options

  ```sh
  cookiecutter https://github.com/incoggnito/cookiecutter-pypackage.git
  ```

- `pyenv` to setup different python versions

  ```py
  # Install some python versions.
  pyenv install  3.7.5

  # In the current directory, set the python version. This creates the file .python-version.
  pyenv local 3.7.5
  ```

- `poetry` to manage virtual environments

  ```py
  # Install a new package
  poetry add numba
  ```

- `direnv` to auto activate the virtual environment, [Setup](https://github.com/direnv/direnv/wiki/Python)

  ```sh
  echo "layout poetry" > .envrc
  direnv allow
  ```

- Create a GitHub repository and use `git` commands to link remote
  
  ```sh
  cd my-new-tool
  git init
  git add .
  git commit -m "Initial structure from template"
  # Rename the 'master' branch to 'main':
  git branch -m master main
  ```

- [Register](https://packaging.python.org/tutorials/packaging-projects/#uploading-the-distribution-archives) your project with PyPI
- Add API tokens as GitHub secrets for [PyPI](https://pypi.org/) (`PYPI_API_TOKEN`) and [Test PyPI](https://test.pypi.org/) (`TEST_PYPI_API_TOKEN`) for automated publishing
- Add the repo to your [Read the Docs](https://readthedocs.org/) account and activate the service hook
- Release your package by pushing a new tag to master
