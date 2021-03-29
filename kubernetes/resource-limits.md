## Resource Limits

> Operating params provided to Kubernetes to tell it:
>   - the resources that you require to run properly and,
>   - the maximum resources your workload is allowed to consume.


These params are defined while creating a container, using a `resources` property of the containerSpec.

```yaml
  resources:
    requests:
      cpu: 500m
      memory: 330Mi
    limits:
      cpu: 500m
      memory: 1000Mi
```

The above config defines that, in normal operations, the container needs 330 Mebibytes of ram and should max out at 1000 Mebibytes of ram.

As for CPU requirements, the config defines that the container needs 50% of a core(0.5 cores) and is allowed to use at most 50% of a core.

To determine the resource usage on your namespace via the command line, run:

```shell
$ kubectl get quota -o yaml
```

The output of available quota will include total allowed on the cluster and total used:
```yaml
  spec:
    hard:
      requests.cpu: "35"
      requests.memory: 10Gi
  status:
    hard:
      requests.cpu: "35"
      requests.memory: 10Gi
    used:
      requests.cpu: 19000m
      requests.memory: 5420Mi
```

This means that of the 10Gi allocated on the namespace, we are at approx 50% memory usage and 54% CPU usage.

### Conversion Notes
- For Memory `1024 Mi(Mebibytes) = 1 Gi(Gibibytes)`
- For CPU: `m` stands for `thousandth of a core`, so `2000m` will be `2 cores`.
