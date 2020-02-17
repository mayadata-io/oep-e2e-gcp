# Cleaning up the user k8s cluster created on GCP

The following steps are performed for cleaning up the user kubernetes cluster created on GCP:

- Authorise using SDK token.
- Set google cloud project.
- Clone the mayadata-io litmus repository -- https://github.com/mayadata-io/litmus
- Get into the following directory `litmus/k8s/gcp/k8s-installer/`
- Delete the cluster using the playbook `delete-k8s-cluster.yml`.
- Delete VPC using the playbook `delete-vpc.yml` and pass the project in which the cluster exists as an env variable.