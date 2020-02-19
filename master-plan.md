## File .master-plan.yaml

This file would contain all the desired/known test cases for OEP platform. The schema of this file



```kind: MasterPlan
apiVersion: e2e.mayadata.io/v1alpha1
metadata:
  name: masterTestplan
spec:
  tests:
  ### Installation of OpenEBS
  - tcid: "IUOI01"
    name: "Install OpenEBS on a Onprem Cluster"
    description: "Test the components are installed properly using both backend and Director apis. Check from the status from status agent response for the OpenEBS components."
    labels:
      test/feature: "Install and Upgrade of OpenEBS"
      test/subFeature: "Install OpenEBS ControlPlane"
      test/priority: "P0"
      git/location: "https://github.com/mayadata-io/oep-e2e-gcp"

  - tcid: "IUOI02"
    name: "Install OpenEBS on a K8S Cluster connected to Onprem Cluster"
    description: "Optional skipping here"
    labels:
      test/feature: "Install and Upgrade of OpenEBS"
      test/subFeature: "Install OpenEBS ControlPlane"
      test/priority: "P0"
      git/location: "https://github.com/mayadata-io/oep-e2e-gcp"
```





where 

tcid -- referers to a unique id for the testcase. 

The test case would be called as job in gitlabl pipeline and would be called in gitlab-ci.yaml. Actual test case would be having this unique id prefixed i

Abbreviations of tcid

first two letter indicates the feature

third and fourth letter indicates the sub feature

last two digits give the count of test cases

Example 

Feature

| Feature                   | SubFeature                  |
| ------------------------- | --------------------------- |
| IU -- Install and Upgrade | OI -- OpenEBS Install       |
|                           | OC -- OpenEBS ControlPlane  |
|                           | OD -- OpenEBS DataPlane     |
| TU -- Teaming and Users   | PO -- Project Owner         |
|                           | PA -- Project Admin         |
|                           | PM -- Project Member        |
|                           | PR -- Project ReadOnly User |


