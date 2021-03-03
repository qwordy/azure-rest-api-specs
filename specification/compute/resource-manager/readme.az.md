## AZ

These settings apply only when `--az` is specified on the command line.

``` yaml $(az)
az:
  extensions: cloud-service
  namespace: azure.mgmt.compute
  package-name: azure-mgmt-compute
az-output-folder: $(azure-cli-extension-folder)/src/cloudservice
cli:
    cli-directive:
        - where:
            group: "*"
            op: "*"
          hidden: true
        - where:
            group: "CloudServiceRoleInstances"
            op: "*"
          hidden: false
        - where:
            group: "CloudServiceRoles"
            op: "*"
          hidden: false
        - where:
            group: "CloudServices"
            op: "*"
          hidden: false
        - where:
            group: "CloudServicesUpdateDomain"
            op: "*"
          hidden: false
```