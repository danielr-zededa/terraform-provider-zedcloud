# zedcloud_deployment Data Source

The `zedcloud_deployment` data source retrieves information about a deployment in ZedCloud.

## Example Usage

### Retrieve Deployment by Name and Project ID
```terraform
data "zedcloud_deployment" "example" {
  name       = "my-deployment"
  project_id = "project-123"
}
```

### Retrieve Deployment by ID and Project ID
```terraform
data "zedcloud_deployment" "example" {
  id         = "deployment-456"
  project_id = "project-123"
}
```

## Argument Reference

The following arguments are supported:

- `project_id` - (Required) The ID of the project containing the deployment.
- `name` - (Optional) The name of the deployment. Either `name` or `id` must be specified.
- `id` - (Optional) The ID of the deployment. Either `id` or `name` must be specified.
- `x_request_id` - (Optional) Custom request ID for tracking purposes.

## Attribute Reference

In addition to the arguments above, the following attributes are exported:

- `id` - The ID of the deployment.
- `name` - The name of the deployment.
- `project_id` - The ID of the project.
- `deployment_tag` - The deployment tag.
- `title` - The title of the deployment.
- `revision` - The revision information of the deployment.
- `app_inst_policy` - Application instance policy configuration.
- `device_policy` - Device policy configuration.
- `network_inst_policy` - Network instance policy configuration.
- `volume_inst_policy` - Volume instance policy configuration.
- `cluster_policy` - Cluster policy configuration.
- `edgeview_policy` - EdgeView policy configuration.
- `integration_policy` - Integration policy configuration.

## Import

Deployments cannot be imported using this data source. Use the resource import functionality instead.
