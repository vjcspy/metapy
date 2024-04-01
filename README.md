# Metapy

## Features

- Ruff: Linter https://github.com/astral-sh/ruff


### Creating New Services and Packages
This repository includes a Makefile that provides convenient targets for creating new services and packages.
These targets are implemented using shell scripts located in the scripts directory, and provide boilerplate code and
configuration files to help get started with new projects.

To create a new service, run the new-service target from the command line and provide a name for your service:

```shell
make new-service name=<service-name>
```

This will create a new service directory in the services directory with the provided name.
The directory will contain a Dockerfile for building the service, a pyproject.toml file for listing dependencies,
and a basic project structure.

To create a new package, run the new-package target from the command line and provide a name for your package:

```shell
make new-package name=<package-name>
```

This will create a new Python package in the packages directory with the provided name.
The directory will contain a basic project structure with a pyproject.toml file for listing dependencies.

These targets are designed to help you get started quickly and provide a consistent project structure across all your
services and packages. You can modify the shell scripts to suit your own needs or create your own targets in the
Makefile as needed.

---

## Using the Makefile

This repository includes a Makefile with targets that automate common tasks for Python services.
These targets are implemented using shell scripts located in the scripts directory and can be invoked from the command
line using the make command.

Here are the available targets:

### Installation
This target installs the service and its dependencies into a virtual environment.
It uses Poetry to manage dependencies and installs them according to the configuration in the pyproject.toml file.

To use this target, run the following command from the root directory of your service:
```shell
make install
```

### Code formatting
This target formats the code using Black, a Python code formatter. It applies a consistent coding style to your
codebase and ensures that it follows the PEP 8 guidelines.

To use this target, run the following command from the root directory of your service:

```shell
make format
```

### Linting
This target lints the code using Ruff, a fast Python linter written in Rust. It checks your codebase for syntax errors,
style violations, and potential bugs, and provides a report of any issues found.

To use this target, run the following command from the root directory of your service:
```shell
make lint
```

### Unit testing
This target runs the unit tests for your service using Pytest, a Python testing framework. It discovers and runs all
tests in the tests directory and provides a report of the test results.

To use this target, run the following command from the root directory of your service:
```shell
make test
```
