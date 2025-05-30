# csv-reconcile-fingerprint

[![PyPI](https://img.shields.io/pypi/v/csv-reconcile-fingerprint.svg)](https://pypi.org/project/csv-reconcile-fingerprint/)
[![Tests](https://github.com/cutterkom/csv-reconcile-fingerprint/actions/workflows/test.yml/badge.svg)](https://github.com/cutterkom/csv-reconcile-fingerprint/actions/workflows/test.yml)
[![Changelog](https://img.shields.io/github/v/release/cutterkom/csv-reconcile-fingerprint?include_prereleases&label=changelog)](https://github.com/cutterkom/csv-reconcile-fingerprint/releases)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/cutterkom/csv-reconcile-fingerprint/blob/main/LICENSE)

A scoring plugin for [csv-reconcile](https://github.com/gitonthescene/csv-reconcile) using fingerprint clustering.
It generates a fingerprint of the input string by normalizing, removing punctuation, and sorting unique tokens. Based on the [OpenRefine clustering implementation](https://openrefine.org/docs/technical-reference/clustering-in-depth) and [code from this gist](https://gist.github.com/pietz/d6197f64c34d273a6d456d7b736c028d) by [@pietz](https://github.com/pietz).

The resulting strings are compared with Jaccard distance to output a score between 0 and 100.

## Installation and Usage

Install this library using `pip`:
```bash
pip install csv-reconcile
```

This a plugin to the csv reconciliation plugin. So you just have to install [csv reconcile package](https://github.com/gitonthescene/csv-reconcile) and specify the scorer with '--scorer fingerprint' when initiating the reconciliation service.

## Development

To contribute to this library, first checkout the code. Then create a new virtual environment:
```bash
cd csv-reconcile-fingerprint
python -m venv venv
source venv/bin/activate
```
Now install the dependencies and test dependencies:
```bash
python -m pip install -e '.[test]'
```
To run the tests:
```bash
python -m pytest
```
