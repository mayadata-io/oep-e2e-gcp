# self-connected-cluster check

The following checks are performed on self-connected-cluster:

- Initial common checks:
    - Check if maya-system namespace exists
    - Check if all the client-side components of maya-system are present and healthy
    - check ready status of pods
    - check daemonset status
    - Check `Active` status of connected cluster

