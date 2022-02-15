# memcache-operator

## Description

This operator is a test using [operator-sdk](https://sdk.operatorframework.io/docs/). The main purpose here is to test this sdk, learn to build an operator and keep track of everthing.

## Roadmap
* initialize project :heavy_check_mark:
* create api
* create CI with github action

## Setup project

```
$ operator-sdk init --project-name <name> --repo <url> [--domain <mydomain>]
```


## Create controller
Note : `controller` are the brain of an `operator`, they loop insinde `kubernetes` to apply your desir configuration.

```
$ operator-sdk create api --group <target_group> --version <api_version> --kind <api_kind> --resource --controller
```

