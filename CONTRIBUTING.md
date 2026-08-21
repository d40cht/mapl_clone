# How to Contribute

At this time we do not plan to accept contributions. We encourage forking the
repository and continued development (as permitted by the license).

## Contributor License Agreement

Contributions to this project must be accompanied by a Contributor License
Agreement (CLA). You (or your employer) retain the copyright to your
contribution; this simply gives us permission to use and redistribute your
contributions as part of the project. Head over to
<https://cla.developers.google.com/> to see your current agreements on file or
to sign a new one.

You generally only need to submit a CLA once, so if you've already submitted one
(even if it was for a different project), you probably don't need to do it
again.

## Code Reviews

All submissions, including submissions by project members, require review. We
use GitHub pull requests for this purpose. Consult
[GitHub Help](https://help.github.com/articles/about-pull-requests/) for more
information on using pull requests.

## Running Tests

We use [pytest](https://docs.pytest.org/) for running unit tests. You can run
the test suite using either `uv` (recommended for fast, zero-install execution)
or standard `pip` in a Python virtual environment.

### Using `uv` (No Installation Required)

[uv](https://docs.astral.sh/uv/) can run tests in an isolated, ephemeral
environment without needing manual environment creation or package
installation. Because dev dependencies are defined in `[dependency-groups]`,
`uv` includes them by default:

```bash
# Run all tests
uv run pytest

# Run a specific test file
uv run pytest mapl/clustering_test.py
```

### Using `venv` and `pip`

Alternatively, create a virtual environment, install the package in editable
mode with development dependencies, and run `pytest`:

```bash
# Create and activate a virtual environment
python3 -m venv .venv
source .venv/bin/activate

# Install the package in editable mode with dev dependencies
pip install -e . --group dev
# Or with uv: uv pip install --group dev -e .

# Run tests
pytest

# Run a specific test file
pytest mapl/clustering_test.py
```

## Community Guidelines

This project follows
[Google's Open Source Community Guidelines](https://opensource.google/conduct/).
