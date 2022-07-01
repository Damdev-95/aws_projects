## Bucket Policy 

# ENFORCE ENCRYPTION 
```
{
    "Version": "2012-10-17",
    "Id": "Policy1656668504246",
    "Statement": [
        {
            "Sid": "Stmt1656668500934",
            "Effect": "Deny",
            "Principal": "*",
            "Action": "s3:PutObject",
            "Resource": "arn:aws:s3:::calabs-2023/*",
            "Condition": {
                "StringNotEquals": {
                    "s3:x-amz-server-side-encryption": "AES256"
                }
            }
        }
    ]
}
````

# ENFORCE ACCESS FROM A PARTICULAR IP 

```
{
    "Version": "2012-10-17",
    "Id": "Policy1656668504246",
    "Statement": [
        {
            "Sid": "Stmt1656668500934",
            "Effect": "Deny",
            "Principal": "*",
            "Action": "s3:PutObject",
            "Resource": "arn:aws:s3:::calabs-2023/*",
            "Condition": {
                "NotIpAddresss": {
                    "SourceIpAddress": "192.168.10.10"
                }
            }
        }
    ]
}
```
