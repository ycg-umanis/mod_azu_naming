# Azure Umanis Tagging


[![Build Status](https://dev.azure.com/umanis-consulting/terraform/_apis/build/status/mod_azu_tags?branchName=master)](https://dev.azure.com/umanis-consulting/terraform/_build/latest?definitionId=2&branchName=master) [![Unilicence](https://img.shields.io/badge/licence-The%20Unilicence-green)](LICENCE)

Common Azure Terraform module to normalize tagging on ressources.

# Usage

```hcl
module "umanis_tagging" {
  source = <<path_to_module>>

  location          = "France Central"
  client            = "XY2"
  project           = "1234"
  budget            = "FE4567"
  rgpd_personal     = true
  rgpd_confidential = false
}
```
<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 0.15.0 |

## Providers

No providers.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_budget"></a> [budget](#input\_budget) | Budget code. Must have 6 alphanumeric chars. | `string` | n/a | yes |
| <a name="input_client"></a> [client](#input\_client) | Client code. Must have 3 alphanumeric chars. | `string` | n/a | yes |
| <a name="input_project"></a> [project](#input\_project) | Project code. Must have 4 digits. | `string` | n/a | yes |
| <a name="input_rgpd_confidential"></a> [rgpd\_confidential](#input\_rgpd\_confidential) | Indicates that project contains confidential data | `bool` | n/a | yes |
| <a name="input_rgpd_personal"></a> [rgpd\_personal](#input\_rgpd\_personal) | Indicates that project contains personal data | `bool` | n/a | yes |
| <a name="input_custom_tags"></a> [custom\_tags](#input\_custom\_tags) | Specific tags. | `map(string)` | `{}` | no |
| <a name="input_location"></a> [location](#input\_location) | Azure region were resources are deployed | `string` | `"France Central"` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_tags"></a> [tags](#output\_tags) | Umanis standard tags |
<!-- END_TF_DOCS -->