## Kubernetes 1.6.1

### Upgrading to this Version

Warning: The existing template version _must be_ `v1.2.4-rancher9` or later. Ignoring this will result in data loss. For older templates, please first upgrade to `v1.5.4-rancher1`.

If you are trying to create resiliency planes by labeling your hosts to separate out the data, orchestration and compute planes, you **must** change the plane isolation option to `required`. The host labels, `compute=true`, `orchestration=true` and `etcd=true`, are required on your hosts in order for Kubernetes to successfully launch. By default, `none` is selected and there will be not attempt for plane isolation.

### Plane Isolation

If you set the "Plane Isolation" field to `required`, the host labels, `compute=true`, `orchestration=true` and `etcd=true`, are required on your hosts in order for Kubernetes to successfully launch.

### KubeDNS

KubeDNS is enabled for name resolution as described in the [Kubernetes DNS docs](http://kubernetes.io/docs/admin/dns/). The DNS service IP address is `10.43.0.10`.
