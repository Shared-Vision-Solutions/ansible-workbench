# Ansible Workbench

Ansible Role Development Environment.

(Please see the [cookiecutter documentation](https://cookiecutter.readthedocs.io/) for instructions on how to use this project template.)

##### Master Branch (Follows the latest production tag):
[![ansible-workbench-self-test](https://github.com/niall-byrne/ansible-workbench/workflows/ansible-workbench-self-test/badge.svg?branch=master)](https://github.com/niall-byrne/ansible-workbench/actions)

##### Dev Branch:
[![ansible-workbench-self-test](https://github.com/niall-byrne/ansible-workbench/workflows/ansible-workbench-self-test/badge.svg?branch=dev)](https://github.com/niall-byrne/ansible-workbench/actions)

## About

This template generates a development environment for Ansible Roles with a functional CI/CD template for both Travis CI and Github.

## Requirements
You'll need [Python](https://www.python.org/) 3.9 or later to use this template.

## Quick Start Guide

- `pip install cookiecutter poetry`
- `cookiecutter https://github.com/niall-byrne/ansible-workbench.git`

Give your project a name, and populate the other required template inputs.

Once the templating is finished:
- `cd <your new project director>`
- `poetry shell` (to interact with ansible and molecule inside a virtualenv)

## License

[MPL-2](LICENSE)

## Adding / Removing Dependencies For Your Project

#### Python Dependencies:

Use the [pyproject.toml](./{{cookiecutter.project_slug}}/pyproject.toml) file to store your project dependencies in accordance with [PEP 518](https://www.python.org/dev/peps/pep-0518/) and [Poetry Dependency Management](https://python-poetry.org/docs/pyproject/#dependencies-and-dev-dependencies).

Poetry is leveraged to manage the Python dependencies:
- [Adding Python Packages with Poetry](https://python-poetry.org/docs/cli/#add)
- [Removing Python Packages With Poetry](https://python-poetry.org/docs/cli/#remove)

## Default Installed Python Packages:
| package      | Description                                  |
| ------------ | -------------------------------------------- |
| ansible      | Simple, agentless IT automation              |
| ansible-lint | Checks playbooks for practices and behaviour |
| commitizen   | Standardizes commit messages                 |
| poetry       | Python package manager                       |
| molecule     | Ansible test framework                       |
| yamllint     | Lints yaml configuration files               |

## Third Party Integrations

Integrations with the following third party services are configured during templating:

- [Github Workflows](https://docs.github.com/en/free-pro-team@latest/actions/reference/workflow-syntax-for-github-actions)
  - [workflows](./{{cookiecutter.project_slug}}/.github/workflows)
- [TravisCI](https://travis-ci.com/)
  - [.travis.yml](./{{cookiecutter.project_slug}}/.travis.yml)
