# consul check

The following checks are performed on consul:

- Initial common checks:
    - Check the memory consumption of the nodes. If the memory consumption is greater than 90 percent the check fails.
    - Check the CPU consumption of the nodes. If the CPU consumption is greater than 90 percent the check fails.
    - Check if the consul pod exists and is running or not. If the pod is not running the check fails.

- App specific checks:
    - Check if consul members status is 'alive'
