# sonarr

![Version: 9.0.2](https://img.shields.io/badge/Version-9.0.2-informational?style=flat-square) ![AppVersion: 3.0.4.993](https://img.shields.io/badge/AppVersion-3.0.4.993-informational?style=flat-square)

Smart PVR for newsgroup and bittorrent users

**This chart is not maintained by the upstream project and any issues with the chart should be raised [here](https://github.com/k8s-at-home/charts/issues/new/choose)**

## Source Code

* <https://github.com/Sonarr/Sonarr>
* <https://hub.docker.com/r/linuxserver/sonarr>

## Requirements

Kubernetes: `>=1.16.0-0`

## Dependencies

| Repository | Name | Version |
|------------|------|---------|
| https://k8s-at-home.com/charts/ | common | 3.0.1 |

## TL;DR

```console
helm repo add k8s-at-home https://k8s-at-home.com/charts/
helm repo update
helm install sonarr k8s-at-home/sonarr
```

## Installing the Chart

To install the chart with the release name `sonarr`

```console
helm install sonarr k8s-at-home/sonarr
```

## Uninstalling the Chart

To uninstall the `sonarr` deployment

```console
helm uninstall sonarr
```

The command removes all the Kubernetes components associated with the chart **including persistent volumes** and deletes the release.

## Configuration

Read through the [values.yaml](./values.yaml) file. It has several commented out suggested values.
Other values may be used from the [values.yaml](../common/values.yaml) from the [common library](../common).

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`.

```console
helm install sonarr \
  --set env.TZ="America/New York" \
    k8s-at-home/sonarr
```

Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart.

```console
helm install sonarr k8s-at-home/sonarr -f values.yaml
```

## Custom configuration

N/A

## Values

**Important**: When deploying an application Helm chart you can add more values from our common library chart [here](https://github.com/k8s-at-home/charts/tree/master/charts/common/)

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env | object | `{}` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"linuxserver/sonarr"` |  |
| image.tag | string | `"version-3.0.4.993"` |  |
| ingress.enabled | bool | `false` |  |
| persistence.config.emptyDir | bool | `false` |  |
| persistence.config.enabled | bool | `false` |  |
| persistence.media.emptyDir | bool | `false` |  |
| persistence.media.enabled | bool | `false` |  |
| persistence.media.mountPath | string | `"/media"` |  |
| service.port.port | int | `8989` |  |
| strategy.type | string | `"Recreate"` |  |

## Changelog

All notable changes to this application Helm chart will be documented in this file but does not include changes from our common library. To read those click [here](https://github.com/k8s-at-home/charts/tree/master/charts/common/README.md#Changelog).

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

### [1.0.0]

#### Added

- N/A

#### Changed

- N/A

#### Removed

- N/A

[1.0.0]: #1.0.0

## Support

- See the [Docs](https://docs.k8s-at-home.com/our-helm-charts/getting-started/)
- Open an [issue](https://github.com/k8s-at-home/charts/issues/new/choose)
- Ask a [question](https://github.com/k8s-at-home/organization/discussions)
- Join our [Discord](https://discord.gg/sTMX7Vh) community

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)