# Terraform cloud builder

## Getting started

If you are new to Google Cloud Build, we recommend you start by visiting the [manage resources page](https://console.cloud.google.com/cloud-resource-manager) in the Cloud Console, [enable billing](https://cloud.google.com/billing/docs/how-to/modify-project), [enable the Cloud Build API](https://console.cloud.google.com/flows/enableapi?apiid=cloudbuild.googleapis.com), and [install the Cloud SDK](https://cloud.google.com/sdk/docs/).

[terraform]: https://www.terraform.io/

## Building this builder

To build this builder with the default version, run the following command in this directory.

```bash
gcloud builds submit --config=cloudbuild.yaml
```

To override the builder version for Terraform, run the following command in this directory.
(make sure to update the version and the SHA256 hash with the desired ones).

```bash
gcloud builds submit --config=cloudbuild.yaml --substitutions=_TERRAFORM_VERSION="0.12.29",_TERRAFORM_VERSION_SHA256SUM="872245d9c6302b24dc0d98a1e010aef1e4ef60865a2d1f60102c8ad03e9d5a1d" 
```
