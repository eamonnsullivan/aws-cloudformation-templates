# aws-cloudformation-templates

I'm attempting to learn cloudformation. These are just a collection of templates that I'm experimenting with or using.

## Usage

Change to one of the directories (e.g., `s3`) and run the AWS CLI (v2) like so:

```bash
$ aws --profile home cloudformation create-stack --stack-name BasicS3Example --template-body file:///home/eamonn/git/aws-cloudformation-templates/s3/basic-s3-bucket.yml --parameters file:///home/eamonn/git/aws-cloudformation-templates/s3/basic-s3-bucket-parameters.json
$ aws --profile home cloudformation update-stack --stack-name BasicS3Example --template-body file:///home/eamonn/git/aws-cloudformation-templates/s3/basic-s3-bucket.yml --parameters file:///home/eamonn/git/aws-cloudformation-templates/s3/basic-s3-bucket-parameters.json
```
