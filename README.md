# Python license check action

This GitHub action is helpful to check and manage licenses of required python dependencies using liccheck.

## Workflow integration

You can use this action in a workflow, to check licenses of required python dependencies. It is using the python package [liccheck](https://pypi.org/project/liccheck/).

Example configuration:

```yaml
name: Python license check action

on:
  push:
    branches:
      - main

env:
  DEP_PATH: requirements.txt

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Check out master
        uses: actions/checkout@master

      - name: Python License Check
        uses: aufdenpunkt/python-license-check-action@main
```

### ENV variables

To let the script know, where your `requirements.txt` file located is, you have to set the `DEP_PATH` environment variable. See the example above.

## Workflow customization

See full instructions for [Configuring and managing workflows](https://help.github.com/en/actions/configuring-and-managing-workflows).

For help editing the YAML file, see [Workflow syntax for GitHub Actions](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/workflow-syntax-for-github-actions).
