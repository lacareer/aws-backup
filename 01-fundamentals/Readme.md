<!-- Deployment -->
Deply the resources in the following order:

- one-vpc.yaml at the root of the project
- 01/fundamentals/01-resources.yaml (note that ec2, s3, efs, rds all have backup tag set to true for our Backup Plans in 02-aws-backup.yaml)
- 01/fundamentals/02-aws-backup.yaml

<!-- Creating On-Demand Backups -->

Follow the attached pdf doc or the steps below for creating on-demand backups:

- Head to the AWS Backup Console by typing AWS Backup in the search box.

- In the left menu, click on Protected Resources, your screen should look like this. Click the Create on-demand backup button.

- Set Resource type to EC2, and select the Lab1-EC2 instance shown in the drop-down menu.

- Under the Backup window section, select Create backup now

- Under the Retention period drop-down select Days and enter 3.

- From the Backup vault drop-down select the backup vault you created previously Lab1-Vault.

- In the IAM role section, select Choose an IAM role and select the AWSBackupWorkshopRole role.

- Click the Create on-demand backup button to start the backup.

Repeat the same process above for the DDB, EFS, RDS, and S3 to create an on-demand backup for each.