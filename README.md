# ui-preview-build-action

A GitHub action that builds Storybook's static files and stores them into workflow artifacts.
It's the first action of two "Build -> Deploy" actions.

## Inputs

- `pr` (optional) - PR number. Default: action grabs it from the workflow event.
- `node-version` (optional) - Node.js version used to build static files. Default: 14.

## Example

```yaml
name: Preview Build

on:
  pull_request:

jobs:
  build:
    name: Build
    runs-on: ubuntu-latest
    steps:
    - uses: yandex-cloud/ui-preview-build-action@master
```
