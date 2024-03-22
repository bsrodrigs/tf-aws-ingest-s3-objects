## Usage



<!-- BEGIN_TF_DOCS -->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | 5.42.0 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_lambda_batch_ingestion"></a> [lambda\_batch\_ingestion](#module\_lambda\_batch\_ingestion) | terraform-aws-modules/lambda/aws | n/a |

## Resources

| Name | Type |
|------|------|
| [aws_iam_policy.lambda_exec](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_policy) | resource |
| [aws_iam_policy.snf_policy](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_policy) | resource |
| [aws_iam_role.sfn](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role) | resource |
| [aws_iam_role_policy_attachment.policy_1](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role_policy_attachment) | resource |
| [aws_sfn_state_machine.sfn_state_machine](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/sfn_state_machine) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_bucket_name"></a> [bucket\_name](#input\_bucket\_name) | The target bucket name, where you have your targetr objetcs | `string` | n/a | yes |
| <a name="input_lambda_invoke_max_concurrency"></a> [lambda\_invoke\_max\_concurrency](#input\_lambda\_invoke\_max\_concurrency) | Number of concurrent invocations made by step functions. The bigger the concurrency is the more stress the Opensearch will be expose to. The default value was assigned based on load tests, we strongly recommend to keep this value. | `number` | `5` | no |
| <a name="input_project"></a> [project](#input\_project) | Set the project name. This variable is used to name resources. | `string` | `"ingest-s3-objects"` | no |

## Outputs

No outputs.
<!-- END_TF_DOCS -->