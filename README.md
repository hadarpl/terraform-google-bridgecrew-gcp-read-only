# Bridgecrew GCP ReadOnly Integration
[![Maintained by Bridgecrew.io](https://img.shields.io/badge/maintained%20by-bridgecrew.io-blueviolet)](https://bridgecrew.io)
[![GitHub tag (latest SemVer)](https://img.shields.io/github/tag/bridgecrewio/terraform-google-read-only.svg?label=latest)](https://github.com/bridgecrewio/terraform-google-bridgecrew-read-only/releases/latest)
![Terraform Version](https://img.shields.io/badge/tf-%3E%3D0.12.0-blue.svg)

Implementing this module allows visibility to your project on [Bridgecrew Cloud](https://www.bridgecrew.cloud).

## Module contents
This module enables the APIs that allow us to have visibility into your Google Project
and creates a service account for us to scan that project for misconfigurations.
The service account requires the "Viewer" role in order to function properly.

## Configuration

### Prerequisites
This module requires the cURL library to be installed on your machine. To check if you have cURL installed, type the following command in your terminal:
```shell script
curl --help
```

### Installation
To run this module, supply the name of the company as registered in [Bridgecrew Cloud](https://www.bridgecrew.cloud) as such:
```hcl-terraform
module "bridgecrew-read-only" {
  source           = "bridgecrewio/bridgecrew-gcp-read-only/google"
  org_name         = "acme"
  bridgecrew_token = "YOUR_TOKEN"
}
```