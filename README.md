Download the files and run
### This command Checks Template:

aws cloudformation validate-template \
--template-body file://vpc.yaml

### This command creates stack:

aws cloudformation create-stack --stack-name ec2 --template-body file://ec2.yaml

### This command Updates stack:

aws cloudformation update-stack \
--stack-name vpc-cli \
--template-body file://vpc.yaml


#### 