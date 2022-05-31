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
![image](https://user-images.githubusercontent.com/71001536/171135808-7cd752c4-fc99-4a21-8cef-05f48031a65b.png)

![image](https://user-images.githubusercontent.com/71001536/171136312-6ea56f5d-533d-4780-9af0-1ede69b792e1.png)

![image](https://user-images.githubusercontent.com/71001536/171136644-f31ff92a-854b-4d22-8c88-1b5fc7fdae2a.png)

![image](https://user-images.githubusercontent.com/71001536/171144161-3fc7ad53-f41c-4043-8d20-b927719dc5aa.png)


