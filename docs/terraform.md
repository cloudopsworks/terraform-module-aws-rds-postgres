## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.3 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | n/a |
| <a name="provider_random"></a> [random](#provider\_random) | n/a |
| <a name="provider_time"></a> [time](#provider\_time) | n/a |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_tags"></a> [tags](#module\_tags) | cloudopsworks/tags/local | 1.0.9 |
| <a name="module_this"></a> [this](#module\_this) | terraform-aws-modules/rds/aws | 6.8.0 |

## Resources

| Name | Type |
|------|------|
| [aws_secretsmanager_secret.randompass](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/secretsmanager_secret) | resource |
| [aws_secretsmanager_secret_version.randompass](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/secretsmanager_secret_version) | resource |
| [aws_security_group.this](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/security_group) | resource |
| [aws_vpc_security_group_ingress_rule.this_cidr](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/vpc_security_group_ingress_rule) | resource |
| [aws_vpc_security_group_ingress_rule.this_sg](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/vpc_security_group_ingress_rule) | resource |
| [random_password.randompass](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/password) | resource |
| [time_rotating.randompass](https://registry.terraform.io/providers/hashicorp/time/latest/docs/resources/rotating) | resource |
| [aws_region.current](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/region) | data source |
| [aws_security_group.allow_sg](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/security_group) | data source |
| [aws_security_group.this](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/security_group) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_extra_tags"></a> [extra\_tags](#input\_extra\_tags) | n/a | `map(string)` | `{}` | no |
| <a name="input_is_hub"></a> [is\_hub](#input\_is\_hub) | Establish this is a HUB or spoke configuration | `bool` | `false` | no |
| <a name="input_org"></a> [org](#input\_org) | n/a | <pre>object({<br/>    organization_name = string<br/>    organization_unit = string<br/>    environment_type  = string<br/>    environment_name  = string<br/>  })</pre> | n/a | yes |
| <a name="input_security_groups"></a> [security\_groups](#input\_security\_groups) | Security groups for RDS instance | `any` | `{}` | no |
| <a name="input_settings"></a> [settings](#input\_settings) | Settings for RDS instance | `any` | `{}` | no |
| <a name="input_spoke_def"></a> [spoke\_def](#input\_spoke\_def) | n/a | `string` | `"001"` | no |
| <a name="input_vpc"></a> [vpc](#input\_vpc) | VPC for RDS instance | `any` | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_rds_instance_address"></a> [rds\_instance\_address](#output\_rds\_instance\_address) | n/a |
| <a name="output_rds_instance_arn"></a> [rds\_instance\_arn](#output\_rds\_instance\_arn) | n/a |
| <a name="output_rds_instance_endpoint"></a> [rds\_instance\_endpoint](#output\_rds\_instance\_endpoint) | n/a |
| <a name="output_rds_instance_hosted_zone_id"></a> [rds\_instance\_hosted\_zone\_id](#output\_rds\_instance\_hosted\_zone\_id) | n/a |
| <a name="output_rds_instance_port"></a> [rds\_instance\_port](#output\_rds\_instance\_port) | n/a |
| <a name="output_rds_instance_username"></a> [rds\_instance\_username](#output\_rds\_instance\_username) | n/a |
| <a name="output_rds_password"></a> [rds\_password](#output\_rds\_password) | The password for the RDS instance |
| <a name="output_rds_security_group_ids"></a> [rds\_security\_group\_ids](#output\_rds\_security\_group\_ids) | n/a |
