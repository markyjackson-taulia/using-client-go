# Using client-go

A versioned collection of snippets showing how to use [client-go](https://github.com/kubernetes/client-go/).

Contents:

- [Prerequisites](#prerequisites)
- [Kubernetes 1.7](#kubernetes-17)
- [Kubernetes 1.6](#kubernetes-16)
- [Kubernetes 1.5](#kubernetes-15)

## Prerequisites

The snippets shown here have been tested using Go 1.8 and should also work with Go 1.9 (not tested, yet).

In order to manage dependencies (aka vendoring in Go) we use Go [dep](https://github.com/golang/dep).
If you don't have Go `dep` installed yet, simply do the following:

```
$ go get -u github.com/golang/dep/cmd/dep
$ dep init     # only the first time if no Gopkg.* exist in the project
$ dep ensure   # every time you add/change dependencies
```

Note that if you're new to Go dep and/or dependency management, you might want to read
[Using Go dep as a project maintainer](https://hackernoon.com/using-go-dep-as-a-project-maintainer-641d1f3006d7)
before you proceed.

## Kubernetes 1.7

Use the following in your `Gopkg.toml` file (add it if it doesn't exist, otherwise update it):

```
[[constraint]]
  name = "k8s.io/client-go"
  version = "v4.0.0"

[[constraint]]
  name = "k8s.io/apimachinery"
  branch = "release-1.7"
```

After you've updated your `Gopkg.toml` file, do `dep ensure` and commit it to your repo.

Now you can move on to the [Kubernetes 1.7 snippets](1.7/).

## Kubernetes 1.6

TBD

## Kubernetes 1.5

TBD
