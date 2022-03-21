# node-app-demo01
Node app demo from https://github.com/javahometech/node-app


##Github, Codepipeline, Codebuild

1. Create GitHub repo
2. Create Codebuild project

##Running Docker container

``
docker run 
``

## Codebuild Policy
When creating Codebuild project, add this to the default policy
```
{
    "Action": [
        "ecr:GetAuthorizationToken",
        "ecr:DescribeRepositories",
        "ecr:CreateRepository",
        "ecr:InitiateLayerUpload",
        "ecr:UploadLayerPart",
        "ecr:CompleteLayerUpload",
        "ecr:BatchCheckLayerAvailability",
        "ecr:PutImage",
        "ecs:UpdateService"
    ],
    "Resource": "*",
    "Effect": "Allow"
} 
```


## Docker sample for CodeBuild 

https://docs.aws.amazon.com/codebuild/latest/userguide/sample-docker.html