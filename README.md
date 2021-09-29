# VPC
_To create the staging and production VPCs_

### Variables

 * `projectName` - Project Codename

 ### Files
 * `UAT` -  `VPC_EC2_Instance_With_IPv4_Public_UAT.yml`
 * `PROD` -  `VPC_EC2_Instance_With_IPv4_Public_PROD.yml`

### Running
1. Open the AWS CloudFormation console at (https://console.aws.amazon.com/cloudformation)
2. Create a new stack by using one of the following options:
    * Choose Create Stack. This is the only option if you have a currently running stack.
    * Choose Create Stack on the Stacks page. This option is visible only if you have no running stacks.
3. Choose a stack template:
    * On the Specify template page, choose a stack template by using one of the following options:
        1. `Template is ready`
        2. `Upload a template file`
    * Choose Choose File to select the template file that you want to upload. The template can be a maximum size of 1 MB. Once you have chosen your template, CloudFormation uploads the file and displays the S3 URL.
4. To accept your settings, choose Next, and proceed with specifying the stack name:   
    * `UAT` as the `stack name` when running `VPC_EC2_Instance_With_IPv4_Public_UAT.yml`
    * `PROD` as the `stack name` when running `VPC_EC2_Instance_With_IPv4_Public_PROD.yml`   
5. Specifies the provision failure options for all stack deployments and change set operations.
    * The Roll back all stack resources option will roll back all resources specified in the template when the stack status is `CREATE_FAILED` or `UPDATE_FAILED`.
    * For create operations, the `Preserve successfully provisioned resources` option preserves the state of successful resources, while failed resources will stay in a failed state until the next update operation is performed.
    * For update and change set operations, the `Preserve successfully provisioned` resources option preserve the state of successful resources while rolling back failed resources to the last known stable state. Failed resources will be in an UPDATE_FAILED state. Resources without a last known stable state will be deleted upon the next stack operation.
* You can also set the following advanced options for stack creation.
6. Review the stack creation settings and the estimated cost of your stack, choose Create stack to launch your stack.





