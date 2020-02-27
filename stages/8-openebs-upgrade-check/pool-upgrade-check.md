# pool-upgrade check

The following steps are performed on pool-upgrade:

- Check whether all the pool pods are in `Running` state before starting upgrade
- Upgrade OpenEBS control plane
- Fetch `Running` OpenEBS control plane pods state
- Fetch OpenEBS control plane pods ready status
- Get OpenEBS storage pool details and upgrade OpenEBS data plane
- Check `Success` pools upgrade job status
- Check whether all the pool pods are in `Running` state after upgrading
- After upgrading check pool pod's container status
- Verify OpenEBS version of pools is equal to the desired version (openebs_target_version)
