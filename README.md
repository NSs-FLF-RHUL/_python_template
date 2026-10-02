This is the template repository for Python projects maintained by the NNs-FLF-RHUL organisation.
The template can be used to create a new Python project; and comes with the standard folder structure, placeholder metadata files, and GitHub actions for a Python package pre-configured (subject to project-specific information like the project name).

_Before using the template to create your project repository_, decide on a name for your package / project.
This name should conform to the Python convention of being lowercase, and normally a single word.
However, package names can also include underscore if needs be.
Note that you can rename your repository at any time via the GitHub interface, which is very easy to do.
You can similarly rename any packages your repository contains too, however this might be a rather involved process!

To create a new Python project from this repository:

- Navigate to the repository page on GitHub and select the "Use this template" > "Create a new repository" button in the top-right corner.
  **Do not clone** the repository - this will result in your project overwriting the template!
  Make sure you use the aforementioned "Use this template" button.
- Selecting the "Use this template" button will take you to the repository creation page, with the template option already configured.
  - You can leave "Include all branches" set to "off".
  - You should set the repository owner to be the `NNs-FLF-RHUL` organisation from the "choose an owner" dropdown, if you are creating a new project that will be shared amongst the team.
    If you are starting a personal project, you can set the owner to be yourself.
  - In the box after the repository owner, place the project / repository name you decided on.
  - You can optionally provide a short description of the repository, but this can also be changed / configured after it is created.
  - You must also choose whether the repository should be public or private.
    Unless you are writing any sensitive code, public is the way to go.

Once you've configured these options, GitHub will copy the template into a new repository, and will take you to the page for your new project.
You can then create your own local clone / personal fork of the repository it generates, and begin working on your project.

Note that the repository that the template creates will contain are a number of placeholder fields that need to be correctly filled in for the project's infrastructure to work.
A summary of these is provided below; create a branch that fixes the issues, then open the first pull request of the repository to merge the changes in.

- [ ] Having decided on a package name, rename the `src/deepska` folder to `src/your_package_name`.
- [ ] Configure the following files by replacing the `FIXME` placeholders with the information relevant to your project.
  You can use `CTRL+F` (or the find feature of your editor) to look for the `FIXME` placeholders that need, well, fixing.
  - [ ] `pyproject.toml`
  - [ ] `CITATION.cff`
  - [ ] `mkdocs.yml`
  - [ ] `README.md` (this file!)
  - [ ] `.github/ISSUE_TEMPLATES/bug_report.yml`
  - [ ] `docs/api.md`
- [ ] Replace `deepSKA` with the name of your package in `docs/contributing.md`

Once you have completed the above steps, you can delete all this setup text.
Your `README.md` file should begin with the level-1 header line that starts below (`# FIXME`, or whatever it now reads if you have replaced the placeholder).

<!-- Replace all instances of FIXME in this file with your package name, then delete this line! -->
# FIXME

[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)
[![Tests status][tests-badge]][tests-link]
[![Linting status][linting-badge]][linting-link]
[![Documentation status][documentation-badge]][documentation-link]
[![License][license-badge]](./LICENSE.md)

<!-- prettier-ignore-start -->
[tests-badge]:              https://github.com/NSs-FLF-RHUL/FIXME/actions/workflows/tests.yml/badge.svg
[tests-link]:               https://github.com/NSs-FLF-RHUL/FIXME/actions/workflows/tests.yml
[linting-badge]:            https://github.com/NSs-FLF-RHUL/FIXME/actions/workflows/linting.yml/badge.svg
[linting-link]:             https://github.com/NSs-FLF-RHUL/FIXME/actions/workflows/linting.yml
[documentation-badge]:      https://github.com/NSs-FLF-RHUL/FIXME/actions/workflows/docs.yml/badge.svg
[documentation-link]:       https://github.com/NSs-FLF-RHUL/FIXME/actions/workflows/docs.yml
[license-badge]:            https://img.shields.io/badge/License-GPLv3-blue.svg
<!-- prettier-ignore-end -->

## About

:warning: This package is currently under construction and in pre-release.
The API and features may change suddenly without warning.

### Project Team

Vanessa Graber ([vanessa.graber@rhul.ac.uk](mailto:vanessa.graber@rhul.ac.uk))

## Getting Started

### Prerequisites

<!-- Any tools or versions of languages needed to run code. For example specific Python or Node versions. Minimum hardware requirements also go here. -->

`FIXME` requires Python 3.11.

### Installation

<!-- How to build or install the application. -->

We recommend installing in a project specific virtual environment created using
a environment management tool such as
[Conda](https://docs.conda.io/projects/conda/en/stable/). To install the latest
development version of `FIXME` using `pip` in the currently active
environment run

```sh
pip install git+https://github.com/NSs-FLF-RHUL/FIXME.git
```

Alternatively create a local clone of the repository with

```sh
git clone https://github.com/NSs-FLF-RHUL/FIXME.git
```

and then install in editable mode by running

```sh
pip install -e .
```

### Running Locally

### Running Tests

<!-- How to run tests on your local system. -->

Tests can be run across all compatible Python versions in isolated environments
using [`tox`](https://tox.wiki/en/latest/) by running

```sh
tox
```

To run tests manually in a Python environment with `pytest` installed run

```sh
pytest tests
```

again from the root of the repository.

### Building Documentation

The MkDocs HTML documentation can be built locally by running

```sh
tox -e docs
```

from the root of the repository. The built documentation will be written to
`site`.

Alternatively to build and preview the documentation locally, in a Python
environment with the optional `docs` dependencies installed, run

```sh
mkdocs serve
```
