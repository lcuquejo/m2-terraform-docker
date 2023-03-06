# m2-terraform-docker
A terraform wrapper for Macbooks m1/m2 Using docker.

## Env Needed for AWS
AWS_ACCESS_KEY_ID

AWS_SECRET_ACCESS_KEY

TERRAFORM_VERSION (The default value is 0.14.11)

## Extra ENVs
### (BASE_TERRAFORM)
If you have Terraform modules located outside of your current working directory (PWD), you will need to set the BASE_TERRAFORM environemtn. For example, consider the following directory structure:
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
 In this example, If you need to run terraform ini|plan|apply from dev folder, terraform will need to have access to ../../modules, than you need to set the BASE_TERRAFROM as ~/myTerrafom.

```
 export BASE_TERRAFORM=~/myTerraform/
``` 

## How to install:
```
git clone https://github.com/lcuquejo/m2-terraform-docker.git
cp -Rp m2-terraform-docker/terraform /usr/local/bin
```
