# m2-terraform-docker
A terraform wrapper for Macbooks m1/m2 Using docker. Old terraform versions don't have arm binaries so using tfenv will not work.

## Env Needed for AWS
AWS_ACCESS_KEY_ID

AWS_SECRET_ACCESS_KEY

TERRAFORM_VERSION (The default value is 1.5.5)

## Extra ENVs
### (BASE_TERRAFORM)
If you have Terraform modules located outside of your current working directory (PWD), you must set the BASE_TERRAFORM environment. 
For example, consider the following directory structure:
```
.
 └── ~/
     └── myTerraform/
         ├── modules
         └── envs/
             ├── prod
             ├── dev
             └── stg
```
 In this example, If you need to run terraform ini|plan|apply from dev folder, terraform will need to have access to ../../modules, then you need to set the BASE_TERRAFROM as ~/myTerrafom.

```
 export BASE_TERRAFORM=~/myTerraform/
``` 

## How to install:
```
git clone https://github.com/lcuquejo/m2-terraform-docker.git
cp -Rp m2-terraform-docker/terraform /usr/local/bin
```
