# salesforce-build-template
[Build Template for CLI based migration from Git to ANT and Viceversa]

## Highlights:
- No desktop installation for any developer
- Only one-time setup
- Easy maintenance
- Track your builds in clicks
- Your crendetials are stored in a safe place

## Technology or Stack behind
- ANT
	- ant-contrib libray
	- salesforce migration library
- TravisCI

## How it works?

Code -> Git -> Travis Build -> Deployed to Salesforce

#### As a developer, all you need to take care is, deploy the code to Git
Git contains .yml file with build instructions, which contains
- Install a VM Machine
- Run ANT command

#### The ANT Command includes the complete lifecycle
- It compares what was pushed or changed in last deployment
- It moves files from the source(src) folder to target(target) folder
- It then runs deployment from the target with the newly created package
- The credentials required are taken from TravisCI
- You get success or failure messages at the end of the build

#### Future plans
- To include tests for production deployments
- Plan release cycle
