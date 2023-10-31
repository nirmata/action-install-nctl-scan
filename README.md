# action-install-nctl-scan GitHub Action

This action enables you to install nctl.

# Usage

This action currently supports GitHub-provided Linux runner.

Example

```yaml
jobs:
  example:
    runs-on: ubuntu-latest

    permissions: {}

    name: Install NCTL scan
    steps:
      - name: Checkout code
        uses: actions/checkout@v2
        with:
          token: ${{ secrets.PAT }}
          release: 3.3.6
      - name: Install NCTL scan
        uses: ./
      - name: Check install
        run: nctl version
```