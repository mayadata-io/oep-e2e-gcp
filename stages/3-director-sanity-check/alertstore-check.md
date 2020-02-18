# alertstore check

The following checks are performed on alertstore:

- Initial common checks:
    - Check the memory consumption of the nodes. If the memory consumption is greater than 90 percent the check fails.
    - Check the CPU consumption of the nodes. If the CPU consumption is greater than 90 percent the check fails.
    - Check if the alertstore pod exists and is running or not. If the pod is not running the check fails.



| Job ID |   Test Description         | Execution Time |Test Result   |
 |---------|---------------------------| --------------|--------|
 |    <a href= "https://gitlab.mayadata.io/oep/oep-e2e-gcp/-/jobs/37796">37796</a>   |  Common sanity check for alerstore           |  Tue Feb 18 11:19:44 UTC 2020     |Pass  |
