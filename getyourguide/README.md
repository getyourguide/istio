# Build patched images

## Pilot

1.  Disabled strict mTLS cross network endpoints (<https://github.com/istio/istio/pull/26486>)
    -   This is temporary during the clusters migration period.

```shell
export HUBS=130607246975.dkr.ecr.eu-central-1.amazonaws.com/sre
export TAG=1.10.2-patched
sudo TAG=${TAG} HUBS=${HUBS} make dockerx.pilot
docker push ${HUBS}/pilot:${TAG}
```
