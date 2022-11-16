# terraform-aws-vpc-endpoint

[![Lint Status](https://github.com/tothenew/terraform-aws-vpc-endpoint/workflows/Lint/badge.svg)](https://github.com/tothenew/terraform-aws-vpc-endpoint/actions)
[![LICENSE](https://img.shields.io/github/license/tothenew/terraform-aws-vpc-endpoint)](https://github.com/tothenew/terraform-aws-vpc-endpoint/blob/master/LICENSE)

This is a vpc-endpoint to use for baseline. The default actions will provide updates for section bitween Requirements and Outputs.

The following content needed to be created and managed:
 - Introduction
     - Explaination of module 
     - Intended users
 - Resource created and managed by this module
 - Example Usages

<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.3.0 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >= 3.72 |
| <a name="requirement_kubernetes"></a> [kubernetes](#requirement\_kubernetes) | >= 2.10 |
| <a name="requirement_tls"></a> [tls](#requirement\_tls) | >= 3.0 |

## Providers

No providers.

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_autoscaling_interface"></a> [autoscaling\_interface](#module\_autoscaling\_interface) | ./modules/vpc-endpoint/interface | n/a |
| <a name="module_cloudwatch_logs_interface"></a> [cloudwatch\_logs\_interface](#module\_cloudwatch\_logs\_interface) | ./modules/vpc-endpoint/interface | n/a |
| <a name="module_cloudwatch_monitoring_interface"></a> [cloudwatch\_monitoring\_interface](#module\_cloudwatch\_monitoring\_interface) | ./modules/vpc-endpoint/interface | n/a |
| <a name="module_dynamodb_gateway"></a> [dynamodb\_gateway](#module\_dynamodb\_gateway) | ./modules/vpc-endpoint/gateway | n/a |
| <a name="module_ec2_interface"></a> [ec2\_interface](#module\_ec2\_interface) | ./modules/vpc-endpoint/interface | n/a |
| <a name="module_ec2_messages_interface"></a> [ec2\_messages\_interface](#module\_ec2\_messages\_interface) | ./modules/vpc-endpoint/interface | n/a |
| <a name="module_ecr_api_interface"></a> [ecr\_api\_interface](#module\_ecr\_api\_interface) | ./modules/vpc-endpoint/interface | n/a |
| <a name="module_ecr_dkr_interface"></a> [ecr\_dkr\_interface](#module\_ecr\_dkr\_interface) | ./modules/vpc-endpoint/interface | n/a |
| <a name="module_elb_interface"></a> [elb\_interface](#module\_elb\_interface) | ./modules/vpc-endpoint/interface | n/a |
| <a name="module_lambda_interface"></a> [lambda\_interface](#module\_lambda\_interface) | ./modules/vpc-endpoint/interface | n/a |
| <a name="module_s3_gateway"></a> [s3\_gateway](#module\_s3\_gateway) | ./modules/vpc-endpoint/gateway | n/a |
| <a name="module_secrets_manager_interface"></a> [secrets\_manager\_interface](#module\_secrets\_manager\_interface) | ./modules/vpc-endpoint/interface | n/a |
| <a name="module_sns_interface"></a> [sns\_interface](#module\_sns\_interface) | ./modules/vpc-endpoint/interface | n/a |
| <a name="module_sqs_interface"></a> [sqs\_interface](#module\_sqs\_interface) | ./modules/vpc-endpoint/interface | n/a |
| <a name="module_ssm_interface"></a> [ssm\_interface](#module\_ssm\_interface) | ./modules/vpc-endpoint/interface | n/a |
| <a name="module_ssm_messages_interface"></a> [ssm\_messages\_interface](#module\_ssm\_messages\_interface) | ./modules/vpc-endpoint/interface | n/a |

## Resources

No resources.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_cidr_block"></a> [cidr\_block](#input\_cidr\_block) | IPV4 range for VPC Creation | `string` | n/a | yes |
| <a name="input_common_tags"></a> [common\_tags](#input\_common\_tags) | A map to add common tags to all the resources | `map(string)` | n/a | yes |
| <a name="input_environment"></a> [environment](#input\_environment) | n/a | `string` | n/a | yes |
| <a name="input_private_dns_enabled"></a> [private\_dns\_enabled](#input\_private\_dns\_enabled) | n/a | `bool` | n/a | yes |
| <a name="input_profile"></a> [profile](#input\_profile) | A string value for tag as Project Name | `string` | n/a | yes |
| <a name="input_project"></a> [project](#input\_project) | A string value for tag as Project Name | `string` | n/a | yes |
| <a name="input_project_name_prefix"></a> [project\_name\_prefix](#input\_project\_name\_prefix) | A string value to describe prefix of all the resources | `string` | n/a | yes |
| <a name="input_region"></a> [region](#input\_region) | n/a | `string` | n/a | yes |
| <a name="input_route_table_ids"></a> [route\_table\_ids](#input\_route\_table\_ids) | A list of string value for Route table IDs | `list(string)` | n/a | yes |
| <a name="input_security_group_id"></a> [security\_group\_id](#input\_security\_group\_id) | n/a | `string` | n/a | yes |
| <a name="input_subnet_ids"></a> [subnet\_ids](#input\_subnet\_ids) | A list of string value for Subnet IDs | `list(string)` | n/a | yes |
| <a name="input_vpc_id"></a> [vpc\_id](#input\_vpc\_id) | A string value for VPC ID | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_autoscaling_interface_arn"></a> [autoscaling\_interface\_arn](#output\_autoscaling\_interface\_arn) | n/a |
| <a name="output_autoscaling_interface_id"></a> [autoscaling\_interface\_id](#output\_autoscaling\_interface\_id) | n/a |
| <a name="output_cloudwatch_logs_interface_arn"></a> [cloudwatch\_logs\_interface\_arn](#output\_cloudwatch\_logs\_interface\_arn) | n/a |
| <a name="output_cloudwatch_logs_interface_id"></a> [cloudwatch\_logs\_interface\_id](#output\_cloudwatch\_logs\_interface\_id) | n/a |
| <a name="output_cloudwatch_monitoring_interface_arn"></a> [cloudwatch\_monitoring\_interface\_arn](#output\_cloudwatch\_monitoring\_interface\_arn) | n/a |
| <a name="output_cloudwatch_monitoring_interface_id"></a> [cloudwatch\_monitoring\_interface\_id](#output\_cloudwatch\_monitoring\_interface\_id) | n/a |
| <a name="output_dynamodb_gateway_arn"></a> [dynamodb\_gateway\_arn](#output\_dynamodb\_gateway\_arn) | n/a |
| <a name="output_dynamodb_gateway_id"></a> [dynamodb\_gateway\_id](#output\_dynamodb\_gateway\_id) | n/a |
| <a name="output_ec2_interface_arn"></a> [ec2\_interface\_arn](#output\_ec2\_interface\_arn) | n/a |
| <a name="output_ec2_interface_id"></a> [ec2\_interface\_id](#output\_ec2\_interface\_id) | n/a |
| <a name="output_ec2_messages_interface_arn"></a> [ec2\_messages\_interface\_arn](#output\_ec2\_messages\_interface\_arn) | n/a |
| <a name="output_ec2_messages_interface_id"></a> [ec2\_messages\_interface\_id](#output\_ec2\_messages\_interface\_id) | n/a |
| <a name="output_ecr_api_interface_arn"></a> [ecr\_api\_interface\_arn](#output\_ecr\_api\_interface\_arn) | n/a |
| <a name="output_ecr_api_interface_id"></a> [ecr\_api\_interface\_id](#output\_ecr\_api\_interface\_id) | n/a |
| <a name="output_ecr_dkr_interface_arn"></a> [ecr\_dkr\_interface\_arn](#output\_ecr\_dkr\_interface\_arn) | n/a |
| <a name="output_ecr_dkr_interface_id"></a> [ecr\_dkr\_interface\_id](#output\_ecr\_dkr\_interface\_id) | n/a |
| <a name="output_elb_interface_arn"></a> [elb\_interface\_arn](#output\_elb\_interface\_arn) | n/a |
| <a name="output_elb_interface_id"></a> [elb\_interface\_id](#output\_elb\_interface\_id) | n/a |
| <a name="output_lambda_interface_arn"></a> [lambda\_interface\_arn](#output\_lambda\_interface\_arn) | n/a |
| <a name="output_lambda_interface_id"></a> [lambda\_interface\_id](#output\_lambda\_interface\_id) | n/a |
| <a name="output_s3_gateway_arn"></a> [s3\_gateway\_arn](#output\_s3\_gateway\_arn) | n/a |
| <a name="output_s3_gateway_id"></a> [s3\_gateway\_id](#output\_s3\_gateway\_id) | n/a |
| <a name="output_secrets_manager_interface_arn"></a> [secrets\_manager\_interface\_arn](#output\_secrets\_manager\_interface\_arn) | n/a |
| <a name="output_secrets_manager_interface_id"></a> [secrets\_manager\_interface\_id](#output\_secrets\_manager\_interface\_id) | n/a |
| <a name="output_sns_interface_arn"></a> [sns\_interface\_arn](#output\_sns\_interface\_arn) | n/a |
| <a name="output_sns_interface_id"></a> [sns\_interface\_id](#output\_sns\_interface\_id) | n/a |
| <a name="output_sqs_interface_arn"></a> [sqs\_interface\_arn](#output\_sqs\_interface\_arn) | n/a |
| <a name="output_sqs_interface_id"></a> [sqs\_interface\_id](#output\_sqs\_interface\_id) | n/a |
| <a name="output_ssm_interface_arn"></a> [ssm\_interface\_arn](#output\_ssm\_interface\_arn) | n/a |
| <a name="output_ssm_interface_id"></a> [ssm\_interface\_id](#output\_ssm\_interface\_id) | n/a |
| <a name="output_ssm_messages_interface_arn"></a> [ssm\_messages\_interface\_arn](#output\_ssm\_messages\_interface\_arn) | n/a |
| <a name="output_ssm_messages_interface_id"></a> [ssm\_messages\_interface\_id](#output\_ssm\_messages\_interface\_id) | n/a |
<!-- END_TF_DOCS -->

## Authors

Module managed by [TO THE NEW Pvt. Ltd.](https://github.com/tothenew)

## License

Apache 2 Licensed. See [LICENSE](https://github.com/tothenew/terraform-aws-vpc-endpoint/blob/main/LICENSE) for full details.
