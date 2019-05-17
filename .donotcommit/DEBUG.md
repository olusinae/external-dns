# Run locally with a localkubernetes cluster

set KUBERNETES_MASTER to the master URL

```shell
export KUBERNETES_MASTER=https://localhost:6443
```

Run external-dns

```shell
build/external-dns --registry txt --txt-owner-id docker-for-desktop --provider aws --source istio-gateway --log-level=debug --domain-filter=dummy.com
```