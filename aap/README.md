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

[Vaulted](./vars/vaulted.yml) vars
```
# See https://github.com/redhat-cop/infra.aap_configuration/tree/devel/roles/controller_license
# for example using a manifest

# Below uses RH account to lookup and use available subscriptions
vault_rh_username: <Red Hat account username>
vault_rh_password: <Red Hat account password>
```