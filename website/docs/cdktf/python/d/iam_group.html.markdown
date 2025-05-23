---
subcategory: "IAM (Identity & Access Management)"
layout: "aws"
page_title: "AWS: aws_iam_group"
description: |-
  Get information on a Amazon IAM group
---


<!-- Please do not edit this file, it is generated. -->
# Data Source: aws_iam_group

This data source can be used to fetch information about a specific
IAM group. By using this data source, you can reference IAM group
properties without having to hard code ARNs as input.

## Example Usage

```python
# DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import TerraformStack
#
# Provider bindings are generated by running `cdktf get`.
# See https://cdk.tf/provider-generation for more details.
#
from imports.aws.data_aws_iam_group import DataAwsIamGroup
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
        DataAwsIamGroup(self, "example",
            group_name="an_example_group_name"
        )
```

## Argument Reference

* `group_name` - (Required) Friendly IAM group name to match.

## Attribute Reference

This data source exports the following attributes in addition to the arguments above:

* `arn` - Group ARN.
* `group_id` - Stable and unique string identifying the group.
* `id` - Stable and unique string identifying the group.
* `path` - Path to the group.
* `users` - List of objects containing group member information. See below.

### `users`

* `arn` - User ARN.
* `path` - Path to the IAM user.
* `user_id` - Stable and unique string identifying the IAM user.
* `user_name` - Name of the IAM user.

<!-- cache-key: cdktf-0.20.8 input-77c0dae2fedddf6268bb8efcac752894f2507bca79a4d6c27fcd4c551d06b60e -->