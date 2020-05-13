Download the files and run
### This command Checks Template:
cfn-lint -t ec2.yaml


aws cloudformation validate-template \
--template-body file://ec2.yaml

### This command creates stack:

aws cloudformation create-stack --stack-name ec2 --template-body file://ec2.yaml

### This command Updates stack:

aws cloudformation update-stack \
--stack-name vpc-cli \
--template-body file://vpc.yaml


#### Run command with params

aws cloudformation create-stack  --stack-name public-ec2 \
    --template-body file://ec2.yaml \
    --parameters  ParameterKey=SubnetType,ParameterValue=PublicSubnet 






aws cloudformation create-stack  --stack-name public-ec2-cli \
    --template-body file://ec2.yaml \
    --parameters  file://params.json 









#### 
aws cloudformation package --template-file MacroTemplate.yaml \
--s3-bucket macro-test01  --output-template-file packaged-template.yaml