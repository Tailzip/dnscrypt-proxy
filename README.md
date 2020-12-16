# dnscrypt-proxy

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.0.44](https://img.shields.io/badge/AppVersion-2.0.44-informational?style=flat-square)

Simple Helm chart for [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy).

## Usage

### Add Helm repository

```sh
helm repo add tailzip https://tailzip.github.io/dnscrypt-proxy/
helm repo update
```

### Install chart

```sh
helm install --name your-release tailzip/dnscrypt-proxy
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| clusterDomain | string | `""` | used for Helm chart testing only (see [test-dns-proxy.yaml](./charts/dnscrypt-proxy/templates/tests/test-dns-proxy.yaml)) |
| config | string | `""` | dnscrypt-proxy TOML configuration ([see docs](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Configuration)) |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"klutchell/dnscrypt-proxy"` |  |
| image.tag | string | `"2.0.44"` |  |
| nodeSelector | object | `{}` |  |
| resources | object | `{}` |  |
| serviceTCP.annotations | object | `{}` |  |
| serviceTCP.externalTrafficPolicy | string | `"Local"` |  |
| serviceTCP.loadBalancerIP | string | `""` |  |
| serviceTCP.type | string | `"NodePort"` |  |
| serviceUDP.annotations | object | `{}` |  |
| serviceUDP.externalTrafficPolicy | string | `"Local"` |  |
| serviceUDP.loadBalancerIP | string | `""` |  |
| serviceUDP.type | string | `"NodePort"` |  |
| tolerations | list | `[]` |  |

## Acknowledgments

Original software is by the DNSCrypt project: <https://dnscrypt.info/>

## License

- Tailzip/dnscrypt-proxy: [MIT License](./LICENSE)
- klutchell/dnscrypt-proxy: [MIT License](https://github.com/klutchell/dnscrypt-proxy/blob/master/LICENSE)
- DNSCrypt/dnscrypt-proxy: [ISC License](https://github.com/DNSCrypt/dnscrypt-proxy/blob/master/LICENSE)
