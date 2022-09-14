# Azure Pipeline templates

This repo contains various templates for Azure Pipelines.

## Usage

```yaml
resources:
  repositories:
    - repository: templates
      type: github
      endpoint: stefanes
      name: stefanes/azure-pipelines

jobs:
  - job:
    steps:
      - template: install-modules.yml@templates
        parameters:
          modules:
            - PSTibber
            - PSGraphite
          allowPrerelease: false
          reinstall: true
```
