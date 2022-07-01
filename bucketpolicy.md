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

## Lifecycle Policy 

S3 lifecycle policies could be very helpful if you are looking for a solution to automatically perform different kinds of actions on the objects you store inside your bucket.

In this lab step, you will define a lifecycle policy for your S3 bucket, it will let objects expire after 90 days and will move objects older than 30 days from the Standard storage class to the One Zone-IA.

![image](https://user-images.githubusercontent.com/71001536/176873942-774732bb-ee84-4021-bc33-2da4ed2f8b30.png)

![image](https://user-images.githubusercontent.com/71001536/176874366-55db64a7-5c08-4d9b-a0fc-d78c991e678b.png)

![image](https://user-images.githubusercontent.com/71001536/176874458-56f0dbe8-6e49-494b-9cdc-2bd781be853d.png)


