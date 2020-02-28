# Cleaning up a k8s cluster on GCP

The following steps are performed for cleaning up a kubernetes cluster on GCP:

- Authorise using SDK token.
- Set google cloud project.
- Clone the mayadata-io litmus repository -- https://github.com/mayadata-io/litmus
- Get into the following directory `litmus/k8s/gcp/k8s-installer/`
- Delete the cluster using the playbook `delete-k8s-cluster.yml`.
- Delete the firewall rule created to allow tcp traffic on port 30380.
- Delete VPC using the playbook `delete-vpc.yml` and pass the project in which the cluster exists as an env variable.
- Get the disks list and delete all the disks attached to the cluster.