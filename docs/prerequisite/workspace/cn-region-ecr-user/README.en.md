---
title: Create ECR user in China region 
weight: 8
---

## Create IAM user with ECR access only in China region (cn-north-1)

1. Go to China region AWS console [https://console.amazonaws.cn/iamv2/home?#/users](https://console.amazonaws.cn/iamv2/home?#/users)

2. Add User, name: `rs-dev-workshop-cn-ecr-user`, check **Programmatic access**
 ![create ecr user](/images/cn-create-ecr-user.png)

3. Chose policy `AmazonEC2ContainerRegistryFullAccess`
 ![ecr user policy](/images/cn-ecr-user-policy.png)
4. Review and Create the user

5. Record the **Access key ID** and **Secret access key**
![ecr-user-secret-key](/images/cn-ecr-user-secret-key.png)

6. In cloud9 terminal, execute below commands:
```sh 
CN_AWS_ACCESS_KEY_ID=<the Access key ID>
CN_AWS_SECRET_ACCESS_KEY=<the Secret access key>

aws ssm put-parameter --type SecureString --name gcr-rs-dev-workshop-CN_AWS_ACCESS_KEY_ID  --value $CN_AWS_ACCESS_KEY_ID
aws ssm put-parameter --type SecureString --name gcr-rs-dev-workshop-CN_AWS_SECRET_ACCESS_KEY --value $CN_AWS_SECRET_ACCESS_KEY

```