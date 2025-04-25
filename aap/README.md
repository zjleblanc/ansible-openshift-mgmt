# Ansible Automation Platform on OCP

Ansible content related to running AAP on OCP.

## operator_install

### high-level

Deploy and complete initial setup of AAP instance using the Operator
- Create a project/namespace
- Subscribe project to the operator
- Create an instance of AAP
- Readiness checks
- Attach Red Hat subscriptions to the instance

### usage

Important environment vars
```
export K8S_AUTH_HOST="<your_openshift_api_host>"
export K8S_AUTH_API_KEY="<your_openshift_api_key>"
export K8S_AUTH_VERIFY_SSL="false" # optional
```

Playbook vars
```
install_project: <desired project/namespace name> # defaults to ansible-automation-platform
install_name: <desired instance name> # defaults to aap
```