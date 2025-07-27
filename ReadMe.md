markdown
# GitHub Action: gh-first-action

This GitHub Action performs a sample task for demonstration purposes.

## Usage

Add the following to your workflow YAML file:

```yaml
name: Sample Workflow

on:
  push:
    branches:
      - main

jobs:
  sample-job:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v4

      - name: Run gh-first-action
        uses: ./gh-first-action
        with:
          sample-input: 'Hello, World!'