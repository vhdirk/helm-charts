# skooner

![Version: 0.1.4](https://img.shields.io/badge/Version-0.1.4-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: stable](https://img.shields.io/badge/AppVersion-stable-informational?style=flat-square)

Skooner is the easiest way to manage your Kubernetes cluster

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| vhdirk | <vhdirk@gmail.com> | <https://vhdirk.github.io> |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | Configure node affinity |
| deployment.annotations | object | `{}` |  |
| deployment.automountServiceAccountToken | bool | `false` |  |
| deployment.customLivenessProbe | object | `{}` | Configure a custom livenessProbe. This overwrites the default object |
| deployment.customReadinessProbe | object | `{}` | Configure a custom readinessProbe. This overwrites the default object |
| deployment.customStartupProbe | object | `{}` | Configure a custom startupProbe. This overwrites the default object |
| deployment.dnsConfig | object | `{}` | Configure pod dnsConfig. |
| deployment.extraArgs | list | `[]` | Array of extra arguments to be passed down to the Deployment. Kubernetes args format is expected |
| deployment.extraContainers | string | `""` | If you want to add extra sidecar containers. |
| deployment.extraEnv | list | `[]` |  |
| deployment.extraInitContainers | string | `""` | If you want to add extra init containers. |
| deployment.extraVolumeMounts | list | `[]` | Extra volume mounts, allows mounting the extraVolumes to the container. |
| deployment.extraVolumes | list | `[]` | Extra volumes you can attach to the pod. |
| deployment.labels | object | `{}` |  |
| deployment.lifecycle | object | `{}` |  |
| deployment.livenessProbe | object | `{"failureThreshold":5,"initialDelaySeconds":5,"periodSeconds":10}` | Configure the livenessProbe parameters |
| deployment.nodeSelector | object | `{}` | Node labels for pod assignment. |
| deployment.podMetadata | object | `{"annotations":{},"labels":{}}` | Specify pod metadata, this metadata is added directly to the pod, and not higher objects |
| deployment.podMetadata.annotations | object | `{}` | Extra pod level annotations |
| deployment.podMetadata.labels | object | `{}` | Extra pod level labels |
| deployment.resources | object | `{}` |  |
| deployment.serviceAccount | object | `{"annotations":{},"create":true,"name":""}` | Specify the serviceAccountName value. |
| deployment.serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| deployment.serviceAccount.create | bool | `true` | Specifies whether a service account should be created |
| deployment.serviceAccount.name | string | `""` | The name of the service account to use. If not set and create is true, a name is generated using the fullname template |
| deployment.strategy.rollingUpdate | object | `{}` |  |
| deployment.strategy.type | string | `"RollingUpdate"` |  |
| deployment.terminationGracePeriodSeconds | int | `60` |  |
| deployment.tolerations | list | `[]` | Configure node tolerations. |
| fullnameOverride | string | `""` | Full chart name override |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"ghcr.io/skooner-k8s/skooner"` |  |
| image.tag | string | `"stable"` |  |
| imagePullSecrets | list | `[]` | Image pull secrets |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"skooner.localhost"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| nameOverride | string | `""` | Chart name override |
| podSecurityContext.fsGroup | int | `65534` |  |
| podSecurityContext.fsGroupChangePolicy | string | `"OnRootMismatch"` |  |
| podSecurityContext.runAsGroup | int | `65534` |  |
| podSecurityContext.runAsNonRoot | bool | `true` |  |
| podSecurityContext.runAsUser | int | `65534` |  |
| podSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| securityContext.allowPrivilegeEscalation | bool | `false` |  |
| securityContext.capabilities.drop[0] | string | `"ALL"` |  |
| securityContext.privileged | bool | `false` |  |
| securityContext.readOnlyRootFilesystem | bool | `true` |  |
| securityContext.runAsGroup | int | `65534` |  |
| securityContext.runAsNonRoot | bool | `true` |  |
| securityContext.runAsUser | int | `65534` |  |
| securityContext.seLinuxOptions.level | string | `"s0:c123,c456"` |  |
| securityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| service.annotations | object | `{}` | If you do want to specify annotations, uncomment the following lines, adjust them as necessary, and remove the curly braces after 'annotations:'. kubernetes.io/ingress.class: nginx kubernetes.io/tls-acme: "true" |
| service.enabled | bool | `true` | En-/disable the service |
| service.labels | object | `{}` | If you do want to specify additional labels, uncomment the following lines, adjust them as necessary, and remove the curly braces after 'labels:'. e.g.  app: skooner |
| service.loadBalancerIP | string | `""` | The load balancer IP |
| service.name | string | `"http"` | The service port name. Useful to set a custom service port name if it must follow a scheme (e.g. Istio) |
| service.port | int | `4654` | The service port |
| service.type | string | `"ClusterIP"` | The service type |
| skooner.port | int | `4654` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.13.1](https://github.com/norwoodj/helm-docs/releases/v1.13.1)
