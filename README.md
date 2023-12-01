# Helloworld Project Action

This GitHub Action Executes a PowerShell script with parameters, with an option to simulate failures for testing purposes.

## Inputs

### `projectName`

**Required** The name of the project. Used within the script for logging and generating artifacts.

### `simulateFail`

Optional. Set to `true` to simulate a failure in the script. Useful for testing error handling in workflows.

## Outputs

This action does not set any outputs, but it generates an artifact and can be used to demonstrate error handling in a workflow.

## Example Usage

```yaml
jobs:
  build:
    runs-on: windows-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2

      - name: Run PowerShell Project Action
        uses: benhar-dev/github-action-helloworld@v4
        with:
          projectName: "Your Project Name"
          simulateFail: "false"
```
