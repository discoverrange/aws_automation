# aws_automation

Lamda function
In this we are using boto3 libary, The lamda function will delete the inactive access keys for than 30 days.

Attach the following role to the lamda with the below inline policy
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Action": [
                "iam:ListUsers",
                "iam:ListAccessKeys",
                "iam:GetAccessKeyLastUsed",
                "iam:DeleteLoginProfile",
                "iam:GetAccessKeyLastUsed",
                "iam:ListAccessKeys",
                "iam:ListUsers",
                "iam:GetUser",
                "iam:GetLoginProfile",
                "iam:UpdateAccessKey",
                "logs:CreateLogStream",
                "logs:CreateLogGroup",
                "iam:ListAccountAliases",
                "logs:PutLogEvents",
                "iam:DeleteAccessKey"
            ],
            "Resource": "*",
            "Effect": "Allow"
        }
    ]
}
```
