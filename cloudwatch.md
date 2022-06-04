## CloudWatch Logs 


# logs policy
```
{

    "Version": "2012-10-17",

    "Statement": [

        {

            "Action": [

                "logs:CreateLogGroup",

                "logs:CreateLogStream",

                "logs:PutLogEvents",

                "logs:DescribeLogGroups",

                "logs:Describe*",

                "logs:DescribeLogStreams"

            ],

            "Effect": "Allow",

            "Resource": "*"

        }

    ]

}
```

# Trust policy 
```
{

  "Version": "2012-10-17",

  "Statement": [

    {

      "Sid": "",

      "Effect": "Allow",

      "Principal": {

        "Service": "vpc-flow-logs.amazonaws.com"

      },

      "Action": "sts:AssumeRole"

    }

  ]

}
```


![image](https://user-images.githubusercontent.com/71001536/172000791-3e637de5-587b-488c-8679-1409f8c5f04f.png)

![image](https://user-images.githubusercontent.com/71001536/172003668-7804684d-eacb-4f8d-bef8-e4561fcd2c35.png)

