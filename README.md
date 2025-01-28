# Algorand NodeKit on AWS (CloudFormation)

This repository provides a CloudFormation template to deploy an **Algorand NodeKit node** on AWS. The setup is optimized for **non-archival participation nodes** with minimal cost and effort.

## Features

- **Automated Deployment**: Uses AWS CloudFormation for infrastructure-as-code.
- **Cost-Optimized**: Designed for minimal AWS resource usage.
- **Non-Archival Node**: Requires only 100GB of storage.
- **Quick Start**: Deploys in minutes using the official NodeKit installation script.

## Prerequisites

- AWS account
- EC2 KeyPair
- VPC and Subnet

## Deployment Steps

1. Clone this repository.
2. Deploy the CloudFormation template via the AWS Management Console or CLI.
3. SSH into the instance to verify the node status.

## Usage

- Check node status: `algokit node status`
- Monitor logs: `journalctl -u algorand-nodekit`
- Access metrics: `curl http://<public-ip>:8080/v2/status`

## Cost Estimate

- **EC2 (c6i.2xlarge)**: $312.44/month (on-demand)
- **EBS (100GB gp3)**: $8.00/month
- **Total**: ~$320.44/month

## Contributing

Pull requests are welcome! For major changes, please open an issue first.

## License

[MIT](LICENSE)
