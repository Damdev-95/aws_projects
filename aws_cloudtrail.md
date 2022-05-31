## AWS CloudTrail
Continuously log your AWS account activity, Use CloudTrail to meet your governance, compliance, and auditing needs for your AWS accounts.

CloudTrail stores API calls and activities on the accounts, which include;
* Management events: include activities on the control plance such as creating IAM, EC2 instance, interacting with AWS services on the mangement level
* Data events: include the data events such as Lamdda invocation, SNS AND SQS, interaction between AWS Services.

![image](https://user-images.githubusercontent.com/71001536/171133288-559c1708-27f0-4dad-8b2f-8020db8dbdb6.png)

![image](https://user-images.githubusercontent.com/71001536/171133915-f56f5380-966b-4ce0-b133-0275d6c84ed3.png)

JSON Policy for IAMRole for the CloudTrail to access CloudWatch logs
```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AWSCloudTrailCreateLogStream2014110",
      "Effect": "Allow",
      "Action": [
        "logs:CreateLogStream"
      ],
      "Resource": [
        "arn:aws:logs:us-east-1:014285054687:log-group:CloudTrailRoleForCloudWatchLogs-Douxtech:log-stream:014285054687_CloudTrail_us-east-1*",
        "arn:aws:logs:us-east-1:014285054687:log-group:CloudTrailRoleForCloudWatchLogs-Douxtech:log-stream:o-je4worq6xn_*"
      ]
    },
    {
      "Sid": "AWSCloudTrailPutLogEvents20141101",
      "Effect": "Allow",
      "Action": [
        "logs:PutLogEvents"
      ],
      "Resource": [
        "arn:aws:logs:us-east-1:014285054687:log-group:CloudTrailRoleForCloudWatchLogs-Douxtech:log-stream:014285054687_CloudTrail_us-east-1*",
        "arn:aws:logs:us-east-1:014285054687:log-group:CloudTrailRoleForCloudWatchLogs-Douxtech:log-stream:o-je4worq6xn_*"
      ]
    }
  ]
}
```

