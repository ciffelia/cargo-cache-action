# cargo-cache-action
GitHub Action for caching cargo dependencies

## Example

```yaml
on: [push]

jobs:
  check:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - uses: actions-rs/toolchain@v1
        with:
          toolchain: stable
          override: true

      - uses: ciffelia/cargo-cache-action@v1

      - run: cargo check
```
