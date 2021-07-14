# k3d-knative

Simple knative development environment using k3d. stand up a working
knative serving & eventing environment for development within two minutes.

## Requirements

Below are required for commands to work.

* `go-task`: https://taskfile.dev
* `kn`: https://github.com/knative/client

## Getting Started

> `task bootstrap`

This one single command will give you the following in right around two minutes.

* K3d single node _cluster_
* Knative Operator
* Knative Serving
* Knative Eventing
* Kourier Ingress

## Ingress

The k3d runs loadbalancer and binds to ports `80` and `443` on localhost.
Serving is configured to use the `vcap.me` domain which resolves to `127.0.0.1`
for all subdomains.

## Extras

A few things have quick commands for easy setup

* `task extras:apiserver`: install an `ApiServerSource`
* `task extras:broker`: install a Broker named `default`
* `task extras:display`: install `event-display` that listens to default broker
* `task extras:player`: install `cloudevent-player` that listens to default broker
