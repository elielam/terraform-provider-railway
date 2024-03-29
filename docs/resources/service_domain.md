---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "railway_service_domain Resource - terraform-provider-railway"
subcategory: ""
description: |-
  Railway service domain.
---

# railway_service_domain (Resource)

Railway service domain.

## Example Usage

```terraform
resource "railway_service_domain" "api" {
  subdomain      = "example-api"
  environment_id = railway_project.example.default_environment.id
  service_id     = railway_service.example.id
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `environment_id` (String) Identifier of the environment the service domain belongs to.
- `service_id` (String) Identifier of the service the service domain belongs to.
- `subdomain` (String) Subdomain of the service domain.

### Read-Only

- `domain` (String) Full domain of the service domain.
- `id` (String) Identifier of the service domain.
- `project_id` (String) Identifier of the project the service domain belongs to.
- `suffix` (String) Suffix of the service domain.

## Import

Import is supported using the following syntax:

```shell
terraform import railway_service_domain.api 89fa0236-2b1b-4a8c-b12d-ae3634b30d97:staging:example-api.up.railway.app
```
