# et-service

![Version: 0.1.4](https://img.shields.io/badge/Version-0.1.4-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

A Helm chart for Harness ET Service

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | common | 2.x.x |
| https://harness.github.io/helm-common | harness-common | 1.x.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| env.config.APP_ACL_URL | string | `"https://et-service/gateway/authz/api"` |  |
| env.config.DB_TYPE | string | `"postgresql"` |  |
| env.config.DB_URL | string | `"postgresql:5432"` |  |
| env.config.FRONTEND_URL | string | `"https://et-service/gateway/et"` |  |
| env.config.HEAPDUMP_ON_OOM | bool | `false` |  |
| env.config.HOST_URL | string | `"et-service"` |  |
| env.config.JVM_HEAPSIZE | string | `"6400m"` |  |
| env.secrets.APP_TOKEN_JWT_SECRET | string | `""` |  |
| env.secrets.DBA_USER | string | `"overops"` |  |
| env.secrets.DB_USER | string | `"overops"` |  |
| et.hikari.connectionTimeout | int | `60000` |  |
| et.hikari.maximumPoolSize | int | `50` |  |
| et.hostname | string | `"et-service"` |  |
| et.logLevel | string | `"INFO"` |  |
| et.redis.enabled | bool | `true` |  |
| et.redis.host | string | `"redis-gcp"` |  |
| et.redis.port | int | `6379` |  |
| et.redis.streamLength | int | `1000` |  |
| et.redis.trimCronExpression | string | `"@hourly"` |  |
| fullnameOverride | string | `""` |  |
| image.digest | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.registry | string | `"us.gcr.io"` |  |
| image.repository | string | `"overops-play/overops/et-service"` |  |
| image.tag | string | `"5.2.3-SNAPSHOT-309"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"et-service"` |  |
| ingress.hosts[0].paths[0].backend.serviceName | string | `"et-service"` |  |
| ingress.hosts[0].paths[0].backend.servicePort | int | `9191` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.tls | list | `[]` |  |
| initContainers.check.image.repository | string | `"busybox"` |  |
| initContainers.check.image.tag | string | `"1.33.1"` |  |
| initContainers.postgresql.image.repository | string | `"bitnami/postgresql"` |  |
| initContainers.postgresql.image.tag | string | `"11.10.0-debian-10-r24"` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.failureThreshold | int | `3` |  |
| livenessProbe.initialDelaySeconds | int | `60` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `1` |  |
| maxSurge | string | `"100%"` |  |
| maxUnavailable | int | `0` |  |
| nameOverride | string | `""` |  |
| namespace.name | string | `"overops-snapshot"` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| postgresql.enabled | string | `nil` |  |
| postgresql.hostname | string | `nil` |  |
| postgresql.postgresqlUsername | string | `nil` |  |
| readinessProbe.enabled | bool | `true` |  |
| readinessProbe.failureThreshold | int | `3` |  |
| readinessProbe.initialDelaySeconds | int | `60` |  |
| readinessProbe.periodSeconds | int | `5` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `1` |  |
| replicaCount | int | `1` |  |
| resources.requests.cpu | string | `"100m"` |  |
| resources.requests.memory | string | `"8Gi"` |  |
| securityContext | object | `{}` |  |
| service.port | int | `9191` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| startupProbe.enabled | bool | `true` |  |
| startupProbe.failureThreshold | int | `10` |  |
| startupProbe.initialDelaySeconds | int | `80` |  |
| startupProbe.periodSeconds | int | `10` |  |
| startupProbe.successThreshold | int | `1` |  |
| startupProbe.timeoutSeconds | int | `1` |  |
| tolerations | list | `[]` |  |
| waitForInitContainer.image.digest | string | `""` |  |
| waitForInitContainer.image.pullPolicy | string | `"IfNotPresent"` |  |
| waitForInitContainer.image.registry | string | `"docker.io"` |  |
| waitForInitContainer.image.repository | string | `"harness/helm-init-container"` |  |
| waitForInitContainer.image.tag | string | `"latest"` |  |
