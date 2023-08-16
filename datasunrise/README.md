<h1>
  <img src="https://datasunrise.com/Images/ds-logo-352x352.png" align="left" height="46px" alt="DS logo"/>
  <span>DataSunrise on Kubernetes</span>
</h1>

## Overview
DataSunrise secures databases and data in real-time for all major SQL and NoSQL databases, data-warehouses, and data lakes on AWS.

This is the official Helm chart for installing and configuring DataSunrise on Kubernetes. This chart supports multiple use cases, depending on the values provided.

## Features

- **Proxy functionality:** use a proxy on each node, and Kubernetes will take care of the balancing between them
- **Autoscaling:** use powerful DataDiscovery and new pods will be added to the cluster automatically at the points of the heaviest loads

## Prerequisites
- **Helm 3.6+**
- **Kubernetes 1.21-1.24** - This is the earliest version of Kubernetes tested. It is possible that this chart works with earlier versions, but it has not been fully tested on them.
- **External database for production workloads and HA mode** - This is the recommended way to use the application. It is not necessary in the case of testing. _Supported databases: Postgres, MySQL, MSSQL_

## Usage
To install the latest version of this chart, add the DataSunrise helm repository and run `helm install`:

```console
$ helm repo add datasunrise https://www.datasunrise.com/helm-chart
"datasunrise" has been added to your repositories

$ helm install ds datasunrise/datasunrise
```

Please see the many options supported in the `values.yaml` file.
