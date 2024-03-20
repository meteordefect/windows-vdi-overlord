### Windows VDI Overlord
Creates an EC2 instance from an imported VMWare Windows VM and installs requird VDI components. 

### Import your VM

Import
```
aws ec2 import-image --cli-input-json file://containers.json
```
Check status
```
aws ec2 describe-import-image-tasks --import-task-ids import-ami-12345678
```

Add the resulting AMI to the CloudFormation (CFN) template and run the CFN in your AWS account
```
aws cloudformation describe-stacks --stack-name YourStackName
```

Delete it afterwards
```
aws cloudformation delete-stack --stack-name YourStackName
```


