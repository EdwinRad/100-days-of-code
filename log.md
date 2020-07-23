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
$ What version would you like?(default latest): 1.38.0
$ What dependencies would you like?: s3,iam,ec2,lambda
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

### Day 1: June 01, 2020


**Today's Progress**: Created demo CLI with oclif.

**Thoughts:** dive into nodejs child process to run the commands.

**Link to work:** [DemoCLI](https://github.com/EdwinRad/cdkcli/tree/master/democli/mynewcli)


### Day 2: June 02, 2020


**Today's Progress**: CLI creates installs the CDK in your specified version and creates an empty project.

**Thoughts:** Really good progress. Also found inquirer-autocomplete-prompt Autocomplete prompt for the CLI need to implement this for the dependencies.

**Link to work:** [DemoCLI](https://github.com/EdwinRad/cdkcli/tree/master/democli/mynewcli)


### Day 3: June 03, 2020


**Today's Progress**: Added 'Choose aws-cdk packages to install' to the CLI. 

**Thoughts:** Install latest works, now I need to get the for loop working to install a specific version. See check.ts for code in link below.

**Link to work:** [DemoCLI](https://github.com/EdwinRad/cdkcli/tree/master/democli/mynewcli)


### Day 4: June 04, 2020


**Today's Progress**: CLI now lets you choose a specific package version + combined all steps. 

**Thoughts:** Great progress, took some time to get the for loop working. See init.ts for code in link below.

**Link to work:** [DemoCLI](https://github.com/EdwinRad/cdkcli/tree/master/democli/mynewcli)


### Day 5: June 09, 2020


**Today's Progress**: Added spinner, checkboxes and created new RocketCDK repo 

**Thoughts:** Pretty awesome to see all components come together. The name for the package is now RocketCDK

**Link to work:** [DemoCLI](https://github.com/EdwinRad/cdkcli/tree/master/democli/rocketcdk)

### Day 6: June 10, 2020


**Today's Progress**: Added import to stack.ts writing the packages 

**Thoughts:** Great progress today.

**Link to work:** [DemoCLI](https://github.com/EdwinRad/cdkcli/tree/master/democli/rocketcdk)

### Day 7: June 11, 2020


**Today's Progress**: Published to NPM!

https://www.npmjs.com/package/rocketcdk

**Link to work:** [DemoCLI](https://github.com/EdwinRad/rocketcdk)

### Day 8: June 12, 2020


**Today's Progress**: live bug fixes and writing to  file

**Thoughts:** Great progress today.

**Link to work:** [DemoCLI](https://github.com/EdwinRad/cdkcli/tree/master/democli/rocketcdk)

### Day 9: June 15, 2020


**Today's Progress**: added error handling & wrote the readme


**Link to work:** [RocketCDK npm package](https://www.npmjs.com/package/rocketcdk)

### Day 10: June 16, 2020


**Today's Progress**: worked on website and test deployed with vercel.com


**Link to work:** [RocketCDK npm package](https://www.npmjs.com/package/rocketcdk)

### Day 11: June 23, 2020


**Today's Progress**: added update command to rocketcdk


**Link to work:** [RocketCDK npm package](https://www.npmjs.com/package/rocketcdk)
### Day 12: June 24, 2020


**Today's Progress**: worked on errorhandling


**Link to work:** [RocketCDK npm package](https://www.npmjs.com/package/rocketcdk)

### Day 13: June 26, 2020


**Today's Progress**: corrected error where non empty repo would fail


**Link to work:** [RocketCDK npm package](https://www.npmjs.com/package/rocketcdk)

### Day 14: July 7, 2020


**Today's Progress**: long break but published rocketcdk to version 0.1.1 and looking for fine folks to give feedback.


**Link to work:** [RocketCDK npm package](https://www.npmjs.com/package/rocketcdk)

### Day 15: July 14, 2020


**Today's Progress**: Awesome progress, created the python update model. Better progress then expected.


**Link to work:** [RocketCDK npm package](https://www.npmjs.com/package/rocketcdk)

### Day 16: July 15, 2020


**Today's Progress**: Today I dived into contributing to the AWS CDK. Found a small issue that I want to try and pick up.


**Link to work:** 

### Day 17: July 16, 2020


**Today's Progress**: Added flags to the demoCLI to later add to rocketcdk for using it in pipelines.


**Link to work:** [RocketCDK npm package](https://www.npmjs.com/package/rocketcdk)

### Day 18: July 21, 2020


**Today's Progress**: minor upgrades


**Link to work:** [RocketCDK npm package](https://www.npmjs.com/package/rocketcdk)


### Day 19: July 22, 2020


**Today's Progress**: published version 0.1.2 and added the up command


**Link to work:** [RocketCDK npm package](https://www.npmjs.com/package/rocketcdk)

### Day 20: July 22, 2020


**Today's Progress**: Issues with the rocketcdk and python package on ec2 


**Link to work:** [RocketCDK npm package](https://www.npmjs.com/package/rocketcdk)