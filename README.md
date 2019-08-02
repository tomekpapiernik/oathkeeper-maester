<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [oathkeeper-maester](#oathkeeper-maester)
  - [Prerequisites](#prerequisites)
  - [How to use it](#how-to-use-it)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# oathkeeper-maester

ORY Maester is a Kubernetes controller that watches for instances of `rules.oathkeeper.ory.sh/v1alpha1` custom resource (CR) and creates or updates the Oathkeeper ConfigMap with Access Rules found in the CRs. The controller passes the Access Rules as an array in a format recognized by the Oathkeeper.

The project is based on [Kubebuilder](https://github.com/kubernetes-sigs/kubebuilder)

## Prerequisites

- recent version of Go language with support for modules (e.g: 1.12.6)
- make
- kubectl
- kustomize
- [kind](https://github.com/kubernetes-sigs/kind) for local integration testing
- [ginkgo](https://onsi.github.io/ginkgo/) for local integration testing
- access to K8s environment: minikube or KIND (https://github.com/kubernetes-sigs/kind), or a remote K8s cluster


## How to use it

- `make` to build the binary
- `make test` to run tests
- `make test-integration` to run integration tests with local KIND environment

Other targets require a working K8s environment.
Set `KUBECONFIG` environment variable to the proper value.

- `make install` to generate CRD file from go sources and install it in the cluster
- `make run` to run controller locally

Refer to the Makefile for the details.

