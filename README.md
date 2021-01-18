# aws-cloudformation-templates

I'm attempting to learn cloudformation. These are just a collection of templates that I'm experimenting with or using.

## Usage

Run the AWS CLI (v2) like so:

``` bash
$ aws --profile home cloudformation create-stack --stack-name BasicS3Example \
      --template-body  file:///location/of/basic-s3-bucket.yml \
      --parameters file:///location/of/parameters.json
$ aws --profile home cloudformation update-stack --stack-name BasicS3Example \
      --template-body file:///location/of/basic-s3-bucket.yml \
      --parameters file:///location/of/parameters.json
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
