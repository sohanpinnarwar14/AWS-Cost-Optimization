Project overview - Deleteing the stale snapshots using Lambda function (python + boto3)

Problem statement - In AWS, when an EC2 instance is created, an EBS volume snapshot may also be created for backup purposes.Sometimes, after a few days, a developer deletes the EC2 instance but forgets to delete the snapshots associated with that instance’s EBS volume.
These unused snapshots are called stale snapshots. They remain in the AWS account and continue to consume storage, which increases the AWS cost.To solve this problem, we use an AWS Lambda function written in Python using the Boto3 library. The Lambda function 
automatically identifies and deletes stale EBS snapshots that are not associated with any active EC2 instance. This helps optimize storage usage and reduce AWS costs.


AWS Services Used

Amazon EC2 – To create and manage virtual machines and their associated EBS volumes.

AWS Lambda – To run a Python script that identifies and deletes unused EBS snapshots.

IAM (Identity and Access Management) – To create roles and policies that allow the Lambda function to access EC2 resources and manage snapshots.


