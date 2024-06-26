# astrolabe

Developer tools for testing
[Drivers](https://docs.mongodb.com/ecosystem/drivers/) against [MongoDB
Atlas](https://www.mongodb.com/cloud/atlas). See
[GitHub](https://github.com/mongodb-labs/drivers-atlas-testing) for the
latest source.

## About

The Astrolabe distribution contains tools for automating Atlas
operations and running Atlas Planned Maintenance tests. The
`atlasclient` package provides programmatic access to the [MongoDB Atlas
API](https://docs.atlas.mongodb.com/api/) via a fluent interface. The
`astrolabe` package provides a convenient, command-line interface to the
`atlasclient` and also contains the test harnesses necessary to run
Atlas Planned Maintenance specification tests.

Astrolabe supports Python 3.7+.

## Installation

Astrolabe can be installed with [pip](http://pypi.python.org/pypi/pip):

```bash
python -m pip install astrolabe
```

You can also download the project source and do:

```bash
python -m pip install .
```

## Dependencies

Astrolabe supports CPython 3.7+.

Astrolabe requires [Click](https://pypi.org/project/click/),
[requests](https://pypi.org/project/requests/),
[PyMongo](https://pypi.org/project/pymongo/),
[dnspython](https://pypi.org/project/pymongo/),
[PyYAML](https://pypi.org/project/PyYAML/), and
[junitparser](https://pypi.org/project/junitparser/).

## Documentation

Documentation is available at
[github.io](https://mongodb-labs.github.io/drivers-atlas-testing/).

To build the documentation, you will need to install
[sphinx](https://www.sphinx-doc.org/). Documentation can be generated by
running:

```bash
make html
```

in the `docs/` directory. Generated documentation can be found in the
*docs/build/html/* directory.

## Linting and Formatting

This repo uses [pre-commit](https://pypi.org/project/pre-commit/) for
managing linting. `pre-commit` performs various checks on the files and
uses tools that help follow a consistent style within the repo.

To set up `pre-commit` locally, run:

``` bash
brew install pre-commit
pre-commit install
```

To run `pre-commit` manually, run `pre-commit run --all-files`.

To run a manual hook like `shellcheck` manually, run:

``` bash
pre-commit run --all-files --hook-stage manual shellcheck
```
