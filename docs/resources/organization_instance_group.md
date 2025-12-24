---
layout: "awx"
page_title: "AWX: awx_organization_instance_group"
sidebar_current: "docs-awx-resource-organization_instance_group"
description: |-
  This resource lets you attach or detach an instance group to an organization
---

# awx_organization_instance_group

This resource lets you attach or detach an instance group to an organization

## Example Usage

```hcl
resource "awx_organization" "default" {
    name = "default"
}

resource "awx_instance_group" "default" {
    name = "my-default"
}

resource "awx_organization_instance_group" "default" {
    organization_id   = awx_organization.default.id
    instance_group_id = awx_instance_group.default.id
}
```

## Argument Reference

The following arguments are supported:

* `instance_group_id` - (Required, ForceNew) 
* `organization_id` - (Required, ForceNew) 

