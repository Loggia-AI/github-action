# GitHub Action to Loggia

![https://github.com/loggia-AI/github-action](https://img.shields.io/github/v/release/loggia-AI/github-action)
![https://github.com/loggia-AI/github-action](https://github.com/loggia-AI/github-action/workflows//Publish/badge.svg)

### Usage

| option                     | required | description                |
| -------------------------- | -------- | -------------------------- |
| api-token                  | true     | api token for loggia-ai    |
| test-suite-id              | true     | test suite id              |
| test-suite-environment-url | true     | test suite environment url |

### Example

```yml
name: CI

on: [push]

jobs:
  build:
    name: Test
    runs-on: ubuntu-latest
    steps:
      - name: Run test in Loggia
        uses: loggia-AI/github-action@v1
        with:
          api-token: ${{ secrets.LOGGIA_API_TOKEN }}
          test-suite-id: ${{ secrets.LOGGIA_TEST_SUITE_ID }}
          test-suite-environment-url:
            ${{ secrets.LOGGIA_TEST_SUITE_ENVIRONMENT_URL }}
```

### License

[MIT](./LICENSE)
