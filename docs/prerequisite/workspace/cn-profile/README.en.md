---
title: Config AWS profile to access China region
weight: 6
---
1. In *China region* AWS console, create an IAM user with [policy](https://github.com/gcr-solutions/recommender-system-dev-workshop-code/blob/main/scripts/role/gcr-rs-role.json) 

2. Record the *Access key ID* and *Secret access key*

3. In the Cloud9 terminal, config an AWS profile `rs-dev-workshop-cn` that can access China region (`cn-north-1`) 
```sh 
 aws configure --profile rs-dev-workshop-cn
```
![cn aws profile ](/images/cn-aws-profile.png)



