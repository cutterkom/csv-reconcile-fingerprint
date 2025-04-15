# csv-reconcile-fingerprint

[![PyPI](https://img.shields.io/pypi/v/csv-reconcile-fingerprint.svg)](https://pypi.org/project/csv-reconcile-fingerprint/)
[![Tests](https://github.com/cutterkom/csv-reconcile-fingerprint/actions/workflows/test.yml/badge.svg)](https://github.com/cutterkom/csv-reconcile-fingerprint/actions/workflows/test.yml)
[![Changelog](https://img.shields.io/github/v/release/cutterkom/csv-reconcile-fingerprint?include_prereleases&label=changelog)](https://github.com/cutterkom/csv-reconcile-fingerprint/releases)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/cutterkom/csv-reconcile-fingerprint/blob/main/LICENSE)

A scoring plugin for csv-reconcile using fingerprint clustering.

The resulting strings are compared with Jaccard distance.

## Installation and Usage

Install this library using `pip`:
```bash
pip install csv-reconcile
```

This a plugin to the csv reconciliation plugin. So you just have to install [csv reconcile package]() and specify the scorer with '--scorer fingerprint' when initiating the reconciliation service.

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
