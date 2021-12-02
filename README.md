# AWS-Database-Migration

For this migration, We'll use AWS Database Migration Service (DMS) and many other Services like IAM, EC2, S3 and RDS. 

All of these services mentioned recently can be used under AWS Free Tier which offers some different services from AWS for free, in order to explore many of them.

# Table of Contents  
● [Migrating Data from On-Premise Database to S3](#migratingdatafromonpremise)<br/>
&emsp;◌ [Creating S3 Bucket](#creatings3bucket)<br/>
&emsp;◌ [Creating Postgres RDS](#creatingRDS)<br/>
&emsp;◌ [Launching an EC2 instance](#launchingEC2)<br/>

# Migrating Data from On-Premise Database to S3 <a name="migratingdatafromonpremise"></a>

## Creating S3 Bucket <a name="creatings3bucket"></a>

You can choose two different ways for the s3 bucket creation. It can be done either AWS Management Console or AWS Toolkit for Visual Studio Code.

### AWS Management Console

To create a S3 bucket on Console just look for s3 by typing it.

<img src="https://user-images.githubusercontent.com/69978184/144335790-b755cc37-3e31-4671-8617-c105bb6dd17b.png" width="800" height="400"/>

and then, just click on the orange button which description is "Create Bucket" in order to create bucket.

<img src="https://user-images.githubusercontent.com/69978184/144336501-3de8091d-e40e-4aaa-b7e2-c01f9573d508.png" width="800" height="400"/>

### AWS Toolkit for Visual Studio Code

To do this procedure is needed to install [VS Code](https://code.visualstudio.com/download) on your local Machine.

Once you've installed VSCode, some steps will be needed from now on. 

1) [Obtaining AWS Acess Keys](https://docs.aws.amazon.com/toolkit-for-vscode/latest/userguide/obtain-credentials.html)

2) How to [set up the AWS Credentials](https://docs.aws.amazon.com/toolkit-for-vscode/latest/userguide/setup-credentials.html) on your Local Machine

3) [Connecting to AWS through the AWS Toolkit for Visual Studio Code](https://docs.aws.amazon.com/toolkit-for-vscode/latest/userguide/connect.html)

Once you've already followed the step-by-step guide above, if you acess your VSCode, you may see something like this:

<img src="https://user-images.githubusercontent.com/69978184/144343625-8553c492-8bcf-4a85-8b3e-8567acfcafe7.png" width="800" height="400"/>

It means that the connection between cloud and local machine has been completed Successfully.

Now, you can just click on the bucket object as shown on the image close s3

and then give the bucket name as you want
<img src="https://user-images.githubusercontent.com/69978184/144344451-90440fb8-4511-42b1-8255-f2eae7c4bce4.png" width="800" height="400"/>

The name I chose is dbdmsbucketforcsv as folows

<img src="https://user-images.githubusercontent.com/69978184/144345083-84ab18e9-a6b3-4a17-8937-f24edc7ed764.png" width="800" height="400"/>

As you can see, it was created normally.

## Creating Postgres RDS <a name="creatingRDS"></a>

To create a RDS Database click on Search Console and just look for RDS by typing it.

After that, click on Create Database button

<img src="https://user-images.githubusercontent.com/69978184/144347842-a60ac04c-8154-4826-a923-81abbe72cd6c.png" width="800" height="400"/>

In this step for the creation, be smart with the Postgres version, depending on the version you choose, the free tier is no longer available, that is why you have to be smart when creating this RDS on free tier mode, as follows below

<img src="https://user-images.githubusercontent.com/69978184/144349314-97929957-df27-44ba-9a9a-d3749ed6f879.png" width="800" height="400"/>

and then, keep going by filling those informations required fields. Just notice once you've selected free tier mode, many of these fields will be already filled for this mode mentioned.

<img src="https://user-images.githubusercontent.com/69978184/144349982-4b433035-75f7-4d0b-90d8-4b8d0f195b7e.png" width="800" height="400"/>

then create the database and you will get something like this

<img src="https://user-images.githubusercontent.com/69978184/144350657-3c26f156-3005-4e4b-9b84-4f2badfd68c0.png" width="800" height="400"/>

<img src="https://user-images.githubusercontent.com/69978184/144351554-bd13a3b2-a563-48d9-a282-5f8dff88612f.png" width="800" height="400"/>

## Launching an EC2 instance <a name="launchingEC2"></a>

To create an EC2 instance on Console just look for EC2 by typing it.

After that, just follow this [step-by-step guide](https://www.guru99.com/creating-amazon-ec2-instance.html) to launch an EC2
