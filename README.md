
#### When Workflow Triggers ####

SRP source Provenance submission workflow triggers when any MR merged to master branch.

FYI: Please update workflow with the required branch for which workflow is to be trigger .


#### Steps include in the workflow ####
Print github payload
1. Initialize a ubuntu github runner where workflow steps will run

2. Configure SRP auth secret as environment varriable for Workflow to use (which must have been configured as organizational secret and shared to required repositories)

3. install SRP CLI. (available from as binary file in s3 bucket https://srp-cli.s3.amazonaws.com/srp-cli-latest.tgz)

4. Forms SRP UID for provenance data generation

5. Generate Source provenace data with the well formed SRP UID

6. Publish the provenance data to SRP platform and validate the publishion
