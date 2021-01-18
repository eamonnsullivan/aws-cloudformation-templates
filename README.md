# aws-cloudformation-templates

I'm attempting to learn cloudformation. These are just a collection of templates that I'm experimenting with or using.

## Usage

Change to one of the directories (e.g., `s3`) and run the AWS CLI (v2) like so:

``` bash
$ aws --profile home cloudformation create-stack --stack-name BasicS3Example --template-body file:///home/eamonn/git/aws-cloudformation-templates/s3/basic-s3-bucket.yml --parameters file:///home/eamonn/git/aws-cloudformation-templates/s3/parameters.json
$ aws --profile home cloudformation update-stack --stack-name BasicS3Example --template-body file:///home/eamonn/git/aws-cloudformation-templates/s3/basic-s3-bucket.yml --parameters file:///home/eamonn/git/aws-cloudformation-templates/s3/parameters.json
```

You'll have to provide your own parameters.json. They look like this:

``` json
[
  {
    "ParameterKey": "GithubAccessToken",
    "ParameterValue": "..."
  },
  {
    "ParameterKey": "GithubURL",
    "ParameterValue": "https://github.com/eamonnsullivan/hello-world-example"
  }
]
```

Some of the  stacks need elevated capabilities, for example, the codebuild one. Add `--capabilities CAPABILITY_NAMED_IAM` to the AWS CLI.
