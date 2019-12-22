# Terraform Version Tool
Tool that allows you to easily switch terraform versions.

## Installation
Verify terraform is not installed then run:
```shell script
curl https://raw.githubusercontent.com/Apollorion/tfversiontool/master/terraform > /usr/local/bin/terraform && chmod +x /usr/local/bin/terraform
```

After running the above script, install the latest terraform version with:
```shell script
terraform changeVersion latest
```

You can now use the latest version of terraform:
```shell script
terraform --version
```

## Usage
This tool simply adds the `changeVersion` sub command ontop of terraform itself.  
Syntax: `terraform changeVersion <version>`  
Example: `terraform changeVersion 0.12.5`

After running `changeVersion`, all other subsequent terraform commands will use that version.  
Example:  
```shell script
terraform changeVersion 0.12.11
cd ./prod
terraform init
terraform plan -lock=false
```

This _should_ support pretty much any OS, but has only been tested on mac. If you have any issues feel free to open a PR.