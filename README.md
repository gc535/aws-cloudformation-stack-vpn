# Introduction

This JSON template will create a AWS EC2 instance that can be used as a VPN endpoint. The deployement can be done thru AWS console or CLI. This following instruction shows how it can be done thru the AWS CLI. 

The VPN instance will be created using EC2 along with user data that configures the instance with PPTP/IPSec connection. 

## Usage

This tempalte can be deployed using AWS-CLI tools. 

First, make sure you are in the desired AWS region, which can be configured using:

```bash
aws configure
```

Then, the template can be deployed as cloudformation stack using:
```bash
aws cloudformation update-stack \
  --stack-name brandon-tokyo-vpn \
  --template-body file://full-path-to-this-template-folder/VPN-template.json \
  --tags Key=Scope,Value=vpn
```
## License

[MIT](https://choosealicense.com/licenses/mit/)
