# ng-custom-dashboards

![Version: 0.1.3](https://img.shields.io/badge/Version-0.1.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v1.52.19](https://img.shields.io/badge/AppVersion-v1.52.19-informational?style=flat-square)

A Helm chart for Kubernetes

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | common | 2.x.x |
| https://harness.github.io/helm-common | harness-common | 1.x.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `true` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| config.customerFolderId | string | `"6"` | folder ID of the 'CUSTOMER' folder in looker |
| config.lookerApiVersion | string | `"4.0"` | looker sdk param |
| config.lookerHost | string | `""` | hostname of your looker install |
| config.lookerPort | string | `"80"` | port of your looker install |
| config.lookerScheme | string | `"https"` | scheme used for your looker install, http or https |
| config.lookerTimeout | string | `"120"` | looker sdk param |
| config.lookerVerifySsl | string | `"false"` | looker sdk param |
| config.modelPrefix | string | `""` | if you have configured Looker models with a prefix enter it here |
| config.ootbFolderId | string | `"7"` | folder ID of the 'OOTB' folder in looker |
| config.redisHost | string | `""` | hostname of your redis install |
| config.redisPort | string | `"6379"` | port of your redis install |
| config.redisSentinel | string | `"false"` | used to enable Redis Sentinel support |
| config.redisSentinelMasterName | string | `""` | name of the Redis Sentinel master |
| config.redisSentinelUrls | string | `""` | list of sentinel URLs, example host:port,host:port |
| fullnameOverride | string | `""` |  |
| global.airgap | string | `"false"` |  |
| global.ingress.enabled | bool | `false` |  |
| global.loadbalancerURL | string | `""` |  |
| image.digest | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.registry | string | `"docker.io"` |  |
| image.repository | string | `"harness/dashboard-service-signed"` |  |
| image.tag | string | `"v1.52.19"` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts | string | `nil` |  |
| ingress.tls.enabled | bool | `false` |  |
| ingress.tls.secretName | string | `nil` |  |
| lookerSecrets.clientId.key | string | `"lookerSdkClientId"` |  |
| lookerSecrets.clientId.name | string | `"harness-secrets"` |  |
| lookerSecrets.clientSecret.key | string | `"lookerSdkClientSecret"` |  |
| lookerSecrets.clientSecret.name | string | `"harness-secrets"` |  |
| lookerSecrets.secret.key | string | `"lookerEmbedSecret"` |  |
| lookerSecrets.secret.name | string | `"harness-secrets"` |  |
| maxSurge | int | `1` |  |
| maxUnavailable | int | `0` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| replicaCount | int | `1` |  |
| resources.limits.cpu | int | `1` |  |
| resources.limits.memory | string | `"1536Mi"` |  |
| resources.requests.cpu | int | `1` |  |
| resources.requests.memory | string | `"768Mi"` |  |
| securityContext.runAsNonRoot | bool | `true` |  |
| securityContext.runAsUser | int | `65534` |  |
| service.port | int | `5000` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `false` |  |
| serviceAccount.name | string | `"harness-default"` |  |
| tolerations | list | `[]` |  |

