# actions-poetry-pypi-release
Composite action that releases `mojap` poetry packages to PyPI.

# Example
Assuming your PyPI API token is saved as a GitHub repository secret, then you should be able to run this action as follows:
```
jobs:
    build:
        name: release package to PyPI
        runs-on: ubuntu-latest
        steps:
            - name: checkout repo
              uses: actions/checkout@v3
              with:
                fetch-depth: 1
            - name: release to PyPI
              uses: moj-analytical-services/actions-poetry-pypi-release@v1
              with:
                pypi-api-token: ${{ secrets.PYPI_API_TOKEN }}
```
