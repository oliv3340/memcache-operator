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
**Note :** A `controller` is the brain of an `operator`, they loop insinde `kubernetes` to apply your desir configuration.

```
$ operator-sdk create api --group <target_group> --version <api_version> --kind <api_kind> --resource --controller
```

Then you can start build your api

## Cheatsheet

### Define API
After editing `*_types.go` files run :
```
$ make generate
```
This will generate deepcopy files ensure our API’s Go type definitions implement the `runtime.Object` interface that all Kind types must implement

### Generate CRDs

After API definition run :
```
$ make manifests
```

## Resources
[operator-sdk documentation](https://sdk.operatorframework.io/docs/)
[Groups version and Kinds cheatsheets](https://book.kubebuilder.io/cronjob-tutorial/gvks.html)
