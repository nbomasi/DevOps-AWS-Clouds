# AUTOMATE INFRASTRUCTURE WITH IAC USING TERRAFORM PART 2

This part will introduce us to:

* Terraform backend files: This give us the option of storing local statefile in the cloud, so that other project member can access state file.

* State Locking: it is used to lock your state for all operations that could write state. This prevents others from acquiring the lock and potentially corrupting your state. State Locking feature for S3 backend is optional and requires another AWS service – DynamoDB.

**Steps:**

1. Create a file and name it backend.tf

2. Create DynamoDB
 Apply before the next step
3. Configure S3 Backend

## WORKSPACE VS DIRECTORY

To separate environments with significant configuration differences, use a directory structure. Use workspaces for environments that do not greatly deviate from each other, to avoid duplication of your configurations.


**Resources:**
Configuring backend files: https://angelo-malatacca83.medium.com/aws-terraform-s3-and-dynamodb-backend-3b28431a76c1