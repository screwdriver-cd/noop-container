# noop-container

Bare minimum docker container for running builds

## Usage


### Docker

```
docker run -it --rm screwdrivercd/noop-container bash
```

### Screwdriver

Example `screwdriver.yaml` file

```
jobs:
    main:
        image: screwdrivercd/noop-container
        requires: [~pr, ~commit]
        steps:
            - noop: echo noop
```
