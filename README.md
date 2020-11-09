# Build HTTP API Based Services using Amazon API Gateway, AWS PrivateLink, AWS Fargate and AWS CDK
[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)
[![Gitpod Ready-to-Code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/aws/aws-cdk)
[![NPM version](https://badge.fury.io/js/aws-cdk.svg)](https://badge.fury.io/js/aws-cdk)
[![PyPI version](https://badge.fury.io/py/aws-cdk.core.svg)](https://badge.fury.io/py/aws-cdk.core)
[![NuGet version](https://badge.fury.io/nu/Amazon.CDK.svg)](https://badge.fury.io/nu/Amazon.CDK)

## Architecture
<img width="1042" alt="architecture-screenshot" src="images/Architecture.png">

## Deployment Steps

Pre-requisites:

-	An [AWS account](https://aws.amazon.com/) without any existing transit gateways in us-east-1 or eu-west-1
-	[AWS CLI, authenticated and configured](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
-	[Python 3.6+](https://www.python.org/downloads/)
-	[AWS CDK](https://docs.aws.amazon.com/cdk/latest/guide/getting_started.html)
-	[Git](http://git-scm.com/downloads)

## Prerequisites

Before you build the whole infrastructure, you will need to meet the following pre-requisites.

### AWS account

Ensure you have access to an AWS account, and a set of credentials with *Administrator* permissions. **Note:** In a production environment we would recommend locking permissions down to the bare minimum needed to operate the pipeline.

### Create an AWS Cloud9 environment

Log into the AWS Management Console and search for Cloud9 services in the search bar. Click Cloud9 and create an AWS Cloud9 environment in the `us-east-1` region based on Amazon Linux 2.

### Configure the AWS Cloud environment

Launch the AWS Cloud9 IDE. In a new terminal session, follow the instructions to configure the AWS Cloud9 environment.

![Architecture](images/Cloud9.png)

## Install AWS CDK
`npm install -g aws-cdk`

## Deploy the code samples
   The following commands should be run from the root of the code sample directory.

####   Install AWS CDK packages

   ```bash
   npm install \
  @aws-cdk/aws-elasticloadbalancingv2 \
  @aws-cdk/aws-ec2 \
  @aws-cdk/aws-ecs \
  @aws-cdk/aws-ecr \
  @aws-cdk/aws-iam \
  @aws-cdk/aws-logs \
  @aws-cdk/aws-apigatewayv2
   ```

####   Compile typescript files

  ```bash
  npm run build
  ```
  
#### Bootstrap an environment
```bash
 cdk bootstrap
```

#### Deploy the stack
```bash
 cdk synth
 cdk deploy
```
