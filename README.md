# AWS-Database-Migration

For this migration, We'll use AWS Database Migration Service (DMS) and many other Services like IAM, EC2, S3 and RDS. 

All of these services mentioned recently can be used under AWS Free Tier which offers some different services from AWS for free, in order to explore many of them.

# Table of Contents  
● [Migrating Data from On-Premise Database to S3](#migratingdatafromonpremise)<br/>
&emsp;◌ [Creating S3 Bucket](#creatings3bucket)<br/>

# Migrating Data from On-Premise Database to S3 <a name="migratingdatafromonpremise"></a>

## Creating S3 Bucket <a name="creatings3bucket"></a>

You can choose two different ways for the s3 bucket creation. The first one can be done either AWS Management Console or AWS Toolkit for Visual Studio Code.

### AWS Management Console

To create a S3 bucket on Console just look for s3 by typing it.

<img src="https://user-images.githubusercontent.com/69978184/144335790-b755cc37-3e31-4671-8617-c105bb6dd17b.png" width="700" height="400"/>

and then, just click on the orange button which description is "Create Bucket" in order to create bucket.

<img src="https://user-images.githubusercontent.com/69978184/144336501-3de8091d-e40e-4aaa-b7e2-c01f9573d508.png" width="1000" height="400"/>

### AWS Toolkit for Visual Studio Code

To do this procedure is needed to install [VS Code](https://code.visualstudio.com/download) on your local Machine.

Once you've installed VSCode, some steps will be needed from now on. The First One is how to [set up the AWS Credentials](https://docs.aws.amazon.com/toolkit-for-vscode/latest/userguide/setup-credentials.html) on your Local Machine
