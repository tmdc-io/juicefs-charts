# juicefs-s3-gateway

![Version: 0.10.0](https://img.shields.io/badge/Version-0.10.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.5.0](https://img.shields.io/badge/AppVersion-1.5.0-informational?style=flat-square)

A Helm chart for JuiceFS S3 Gateway

**Homepage:** <https://github.com/juicedata/juicefs>

## Maintainers

| Name           | Email               | Url                   |
|----------------|---------------------|-----------------------|
| Juicedata Inc. | <team@juicedata.io> | <https://juicefs.com> |

## Source Code

* <https://github.com/juicedata/juicefs>

## Values

| Key                                | Type   | Default                    | Description                                                                                                                                                                     |
|------------------------------------|--------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| affinity                           | object | `{}`                       |                                                                                                                                                                                 |
| fullnameOverride                   | string | `""`                       |                                                                                                                                                                                 |
| hostNetwork                        | bool   | `false`                    |                                                                                                                                                                                 |
| image.pullPolicy                   | string | `"IfNotPresent"`           |                                                                                                                                                                                 |
| image.repository                   | string | `"juicedata/mount"`        |                                                                                                                                                                                 |
| image.tag                          | string | `"ce-v1.0.4"`              |                                                                                                                                                                                 |
| imagePullSecrets                   | list   | `[]`                       |                                                                                                                                                                                 |
| ingress.annotations                | object | `{}`                       |                                                                                                                                                                                 |
| ingress.className                  | string | `"nginx"`                  |                                                                                                                                                                                 |
| ingress.enabled                    | bool   | `false`                    |                                                                                                                                                                                 |
| ingress.hosts[0].host              | string | `""`                       |                                                                                                                                                                                 |
| ingress.hosts[0].paths[0].path     | string | `"/"`                      |                                                                                                                                                                                 |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |                                                                                                                                                                                 |
| ingress.tls                        | list   | `[]`                       |                                                                                                                                                                                 |
| metricsPort                        | int    | `9567`                     |                                                                                                                                                                                 |
| nameOverride                       | string | `""`                       |                                                                                                                                                                                 |
| nodeSelector                       | object | `{}`                       |                                                                                                                                                                                 |
| options                            | string | `""`                       | Gateway Options. Separated by spaces. Read [this document](https://juicefs.com/docs/community/command_reference#juicefs-gateway) to learn how to set different gateway options. |
| podAnnotations                     | object | `{}`                       |                                                                                                                                                                                 |
| port                               | int    | `9000`                     |                                                                                                                                                                                 |
| replicaCount                       | int    | `1`                        |                                                                                                                                                                                 |
| resources.limits.cpu               | string | `"5000m"`                  |                                                                                                                                                                                 |
| resources.limits.memory            | string | `"5Gi"`                    |                                                                                                                                                                                 |
| resources.requests.cpu             | string | `"1000m"`                  |                                                                                                                                                                                 |
| resources.requests.memory          | string | `"1Gi"`                    |                                                                                                                                                                                 |
| secret.accessKey                   | string | `""`                       | Access key for object storage                                                                                                                                                   |
| secret.bucket                      | string | `""`                       | Bucket URL. Read [this document](https://juicefs.com/docs/community/how_to_setup_object_storage) to learn how to setup different object storage.                                |
| secret.metaurl                     | string | `""`                       | Connection URL for metadata engine (e.g. Redis). Read [this document](https://juicefs.com/docs/community/databases_for_metadata) for more information.                          |
| secret.name                        | string | `""`                       | The JuiceFS file system name.                                                                                                                                                   |
| secret.secretKey                   | string | `""`                       | Secret key for object storage                                                                                                                                                   |
| secret.storage                     | string | `""`                       | Object storage type, such as `s3`, `gs`, `oss`. Read [this document](https://juicefs.com/docs/community/how_to_setup_object_storage) for the full supported list.               |
| formatOptions                      | string | `""`                       | Format options for JuiceFS. Read [this document](https://juicefs.com/docs/community/command_reference#juicefs-format) to learn how to set different format options.             |
| service.type                       | string | `"ClusterIP"`              |                                                                                                                                                                                 |
| tolerations                        | list   | `[]`                       |                                                                                                                                                                                 |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
