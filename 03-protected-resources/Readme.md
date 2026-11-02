# This lab is a continuation of the previous 02-backup-roles so make sure the infra is still up

# Note: Template should work but was not tested

AWS Backup Audit Manager helps you monitor and evaluate the compliance status of your backups to meet business and regulatory requirements, and enables you to generate reports that help demonstrate compliance to auditors and regulators. In this module we will create a Framework and backup Report.

<!-- B4 deployment -->
# Turn on resource tracking first (aws config resource tracking). Deploy the Lab 4 stack (04-governance) before 03, or enable it from the console under Frameworks > Manage resource tracking. If a recorder already exists, don't deploy 04, because it would conflict.

<!-- Deployment -->
Deply the resources in the following order:

- one-vpc.yaml at the root of the project
- 02-backup-roles/aws-backup.yaml
- 03-protected-resources/aws-backup.yaml