# volume-upgrade check

The following steps are performed on volume-upgrade:

- Check ready state of the OpenEBS control plane pods to make sure that upgrade can be started
- Get the number of CSP and check whether all the pool pods are in running state then check the container status
- Get OpenEBS storage pool details for getting OpenEBS version of pools
- Check application volume health status for all replicas state as `Healthy`
- Get application details for upgrading application volume
- Check application volume upgrade job status as `Success`
- Get cvr list and check `Healthy` status of cvr post upgrading
- Check openebs.io version is equal to desired version (openebs_target_version) in cvr
- Check target pod status post volume upgrade as `Running`
