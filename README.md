# promci-setup

GitHub Action to setup the build environment.

## Usage

```yaml
jobs:
  test:
    name: Go tests
    runs-on: ubuntu-latest
    container:
      image: quay.io/prometheus/golang-builder:1.26-base
    steps:
      - uses: actions/checkout@de0fac2e4500dabe0009e67214ff5f5447ce83dd # v6.0.2
      - uses: prometheus/promci-setup@<sha> # v0.1.0
      - run: make test
```
