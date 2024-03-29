# jdownloader2

![Version: 0.1.3](https://img.shields.io/badge/Version-0.1.3-informational?style=flat-square) ![AppVersion: 23.06.1](https://img.shields.io/badge/AppVersion-23.06.1-informational?style=flat-square)

JDownloader 2 is a free, open-source download management tool with a huge community of developers that makes downloading as easy and fast as it should be. Users can start, stop or pause downloads, set bandwith limitations, auto-extract archives and much more. It's an easy-to-extend framework that can save hours of your valuable time every day!.

**Homepage:** <http://jdownloader.org/>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| vhdirk | <vhdirk@gmail.com> | <https://vhdirk.github.io> |

## Source Code

* <https://hub.docker.com/r/jlesage/jdownloader-2>
* <https://jdownloader.org>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://library-charts.k8s-at-home.com | common | 4.5.2 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env.PGID | string | `"1000"` | Group ID, see PUID |
| env.PUID | string | `"1000"` | User ID of the user you want the container to run as in order to fix folder permission issues |
| env.TZ | string | `"UTC"` | Set the container timezone |
| env.UMASK_SET | string | `"022"` | Default umask for downloaded files |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"jlesage/jdownloader-2"` |  |
| image.tag | string | `"v24.01.1"` |  |
| ingress.main | object | See values.yaml | Enable and configure ingress settings for the chart under this key. |
| persistence | object | See values.yaml | Configure persistence settings for the chart under this key. |
| securityContext.privileged | bool | `false` |  |
| service.main.ports.http.port | int | `5800` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.13.1](https://github.com/norwoodj/helm-docs/releases/v1.13.1)
