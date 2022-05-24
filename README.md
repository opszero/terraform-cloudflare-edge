<!-- BEGIN_TF_DOCS -->
# terraform-cloudflare-domain

Cloudflare Setup for a new SaaS Startup

Includes:

 - Cloudflare Zone
 - Cloudflare SSL Encryption
 - Cloudflare for Teams
 - Gmail
 - AWS SES
 - AWS DynamoDB

 # Deployment

```sh
terraform init
terraform plan
terraform apply -auto-approve
```
# Teardown

```sh
terraform destroy -auto-approve
```
## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | n/a |
| <a name="provider_cloudflare"></a> [cloudflare](#provider\_cloudflare) | n/a |
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_access"></a> [access](#input\_access) | List of access applications | `list` | `[]` | no |
| <a name="input_domain"></a> [domain](#input\_domain) | domain for the webapp | `any` | n/a | yes |
| <a name="input_dynamodb"></a> [dynamodb](#input\_dynamodb) | Specify whether the Dynamodb is enabled | `bool` | `false` | no |
| <a name="input_parking"></a> [parking](#input\_parking) | n/a | `bool` | `false` | no |
| <a name="input_records"></a> [records](#input\_records) | List of DNS records | `list` | `[]` | no |
## Resources

| Name | Type |
|------|------|
| [aws_dynamodb_table.site](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/dynamodb_table) | resource |
| [aws_ses_domain_dkim.dkim](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/ses_domain_dkim) | resource |
| [aws_ses_domain_identity.ses](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/ses_domain_identity) | resource |
| [cloudflare_access_application.access](https://registry.terraform.io/providers/cloudflare/cloudflare/latest/docs/resources/access_application) | resource |
| [cloudflare_access_policy.support_policy](https://registry.terraform.io/providers/cloudflare/cloudflare/latest/docs/resources/access_policy) | resource |
| [cloudflare_page_rule.ssl](https://registry.terraform.io/providers/cloudflare/cloudflare/latest/docs/resources/page_rule) | resource |
| [cloudflare_page_rule.www](https://registry.terraform.io/providers/cloudflare/cloudflare/latest/docs/resources/page_rule) | resource |
| [cloudflare_record.dkim](https://registry.terraform.io/providers/cloudflare/cloudflare/latest/docs/resources/record) | resource |
| [cloudflare_record.mx](https://registry.terraform.io/providers/cloudflare/cloudflare/latest/docs/resources/record) | resource |
| [cloudflare_record.records](https://registry.terraform.io/providers/cloudflare/cloudflare/latest/docs/resources/record) | resource |
| [cloudflare_record.sedo](https://registry.terraform.io/providers/cloudflare/cloudflare/latest/docs/resources/record) | resource |
| [cloudflare_record.ses](https://registry.terraform.io/providers/cloudflare/cloudflare/latest/docs/resources/record) | resource |
| [cloudflare_record.spf](https://registry.terraform.io/providers/cloudflare/cloudflare/latest/docs/resources/record) | resource |
| [cloudflare_worker_route.parking](https://registry.terraform.io/providers/cloudflare/cloudflare/latest/docs/resources/worker_route) | resource |
| [cloudflare_zone.site](https://registry.terraform.io/providers/cloudflare/cloudflare/latest/docs/resources/zone) | resource |
## Outputs

No outputs.
<!-- END_TF_DOCS -->
