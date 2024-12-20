# Bundle Audit Action

This is a GitHub action that runs `bundle-audit check --update`, and then outputs some information about the results. It's designed to be used in conjection with other actions that do something with the results.

See:
- [bundle-audit-check-action](https://github.com/planningcenter/bundle-audit-check-action)
- [bundle-audit-to-asana-action](https://github.com/planningcenter/bundle-audit-to-asana-action)

## Inputs

| Name | Description | Required | Default |
|:-:|:-:|:-:|:-:|
| `ignore_list` | "Space-separated list of CVEs to ignore (e.g., CVE-2023-26141 CVE-2021-41182 CVE-2021-41183)" | false | "" |

## Outputs

| Name | Description |
|:-:|:-:|
| `has_vulnerabilities` | "true" or "false" depending on whether any vulnerabilities were detected |
| `audit_output` | JSON-encoded string containing the vulnerability output |
