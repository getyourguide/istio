# Build patched images

## Pilot

1.  Disabled strict mTLS cross network endpoints (<https://github.com/istio/istio/pull/26486>)
    -   This is temporary during the clusters migration period.

```shell
$ sudo make docker.pilot
$ docker push 130607246975.dkr.ecr.eu-central-1.amazonaws.com/sre/pilot:1.9.3-patched
```
