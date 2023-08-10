# Install AWS Action

[![Tests](https://github.com/aisightgmbh/actions-install-flatc/actions/workflows/on_push.yaml/badge.svg)](https://github.com/aisightgmbh/actions-install-flatc/actions/workflows/on_push.yaml)

This action can be used to install the [Flatbuffers schema compiler](https://flatbuffers.dev/flatbuffers_guide_using_schema_compiler.html).
Afterwards, the `flatc` command will be available to generate source code from *.fbs files.

## Example

```yaml
jobs:
  example-job:
    runs-on: <YourCustomRunner>
    steps:
      - uses: aisightgmbh/actions-install-flatc@v1
      - run: flatc --python --gen-all -o generated/output src/schemas.fbs
```
