# consul check

The following checks are performed on maya-ui:

- Initial common checks:
    - Check the memory consumption of the nodes. If the memory consumption is greater than 90 percent the check fails.
    - Check the CPU consumption of the nodes. If the CPU consumption is greater than 90 percent the check fails.
    - Check if the maya-ui pod exists and is running or not. If the pod is not running the check fails.

- App specific checks:
    - Check admin user login using default credentials. Fails if login not successful i.e, 201 status code not in response of login request sent to "{{ director_url }}/v3/token"
    - Check new user signup. Fails if login not successful i.e, 201 status code not in response of login request sent to "{{ director_url }}/v3/localAuthConfig"
    - Check user login registered in previous check. Fails if login not successful i.e, 201 status code not in response of login request sent to "{{ director_url }}/v3/token"