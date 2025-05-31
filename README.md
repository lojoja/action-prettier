# action-prettier

A composite action that checks file formatting with [Prettier](https://prettier.io).

This repository is not meant to be referenced in third-party workflows; please fork the repository if you would like to use it in your project.

## Inputs

| Name              | Description                                                                                              | Default |
| ----------------- | -------------------------------------------------------------------------------------------------------- | ------- |
| cache             | Whether to cache dependencies.                                                                           | "true"  |
| install           | Whether to install prettier globally. Set to "true" if the repository does not have a package.json file. | "false" |
| node_version      | The node version to use in version spec syntax.                                                          | "22"    |
| working_directory | The working directory for the action.                                                                    | "."     |

## Examples

### With package.json

```
jobs:
  prettier:
    runs-on: ubuntu-latest
    steps:
      - uses: lojoja/action-prettier@main
        with:
          cache: "true"
          node_version: "22"
```

### Without package.json

```
jobs:
  prettier:
    runs-on: ubuntu-latest
    steps:
      - uses: lojoja/action-prettier@main
        with:
          cache: "true"
          install: "true"
          node_version: "22"
```

## License

action-prettier is released under the [MIT License](./LICENSE)
