# AUTOMATE INFRASTRUCTURE WITH IAC USING TERRAFORM PART 2

**This part will introduce us to:**

* Terraform backend files: This give us the option of storing local statefile in the cloud, so that other project member can access state file.

* State Locking: it is used to lock your state for all operations that could write state. This prevents others from acquiring the lock and potentially corrupting your state. State Locking feature for S3 backend is optional and requires another AWS service – DynamoDB.

**Steps:**

1. Create a file and name it backend.tf

2. Create DynamoDB
 Apply before the next step
3. Configure S3 Backend

![programmatic access setup](https://user-images.githubusercontent.com/65962095/216886954-f2f5a4af-a236-4b90-9a5b-c3fabc825ffd.png)


S3 backend configuration image:


![s3-version-page](https://user-images.githubusercontent.com/65962095/216886768-fdc958a5-c66c-4a6d-9926-2ad40b77af34.png)


## WORKSPACE VS DIRECTORY

To separate environments with significant configuration differences, use a directory structure. Use workspaces for environments that do not greatly deviate from each other, to avoid duplication of your configurations.

## CONCEPT OF MODULE

In this part of project, module was introduced, which allows us to break terraform job into smaller piece/module, for easy planning, applying and troubleshooting.
In project18, project17 was broken into 6 modules except for the compute module that was not considered in project 17.

**Image of planned project 18:**
![Project-18](https://user-images.githubusercontent.com/65962095/216886611-507dbe8f-d2c6-4f27-82dd-762161e2552d.png)


**Resources:**
Configuring backend files: https://angelo-malatacca83.medium.com/aws-terraform-s3-and-dynamodb-backend-3b28431a76c1
