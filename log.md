# 100 Days Of Code - Log
## Project: AWS-CDK CLI for quick bootstrapping a new application
# Feature description

As a user I want to be able to use a CLI tool to easily bootstrap a new AWS-CDK project in Typescript.

The core feature is that instead of installing every package standalone with:

```bash
$ npm install @aws-cdk/aws-s3@1.41.1
```

I want to be able to do this in a multi step CLI like:

```bash
$ What language: Typescript
$ What dependencies would you like?: s3,iam,ec2,lambda
$ What version would you like?(default latest): 1.38.0
```

Should result in:

```bash
$ npm install @aws-cdk/aws-s3@1.38.0, aws-cdk/aws-iam@1.38.0, 
aws-cdk/aws-ec2@1.38.0, aws-cdk/aws-lambda@1.38.0
```
## Stretch goal

When the above CLI works I want to add a functionality that will write all imported dependencies from the previous step into the stack.ts:

```tsx
import * as cdk from '@aws-cdk/core';
import * as s3 from '@aws-cdk/aws-s3';
import * as ec2 from '@aws-cdk/aws-ec2';
import * as iam from '@aws-cdk/aws-iam';
import * as lambda from '@aws-cdk/aws-lambda';
```

### Day 1: February 01, 2020


**Today's Progress**: Created demo CLI with oclif.

**Thoughts:** dive into nodejs child process to run the commands.

**Link to work:** [DemoCLI](https://github.com/EdwinRad/cdkcli/tree/master/democli/mynewcli)
