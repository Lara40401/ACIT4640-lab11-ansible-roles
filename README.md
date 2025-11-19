# 4640-ansible-roles-lab

## Getting started

Commands ran:
```
sudo apt update
sudo apt install python3-pip -y
sudo apt install -y python3-boto3
```

Changed the default EC2 instance type from t2.micro to t3.micro to qualify for the free tier: 
    Change the file terraform/modules/web-server/variables.tf:
    ```
        variable "instance_type" {
        description = "The type of EC2 instance"
        type        = string
        default     = "t3.micro" # Default to t2.micro if not specified
        }
    ```
    
Run Playbook by using command: 
```
    ansible-playbook playbook.yml
```
