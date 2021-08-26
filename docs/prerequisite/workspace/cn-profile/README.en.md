---
title: Config AWS profile to access China region
weight: 6
---
1. Go to **China region** AWS console [https://console.amazonaws.cn/iamv2/home?#/users](https://console.amazonaws.cn/iamv2/home?#/users)

2. In create an IAM user with [policy](https://github.com/gcr-solutions/recommender-system-dev-workshop-code/blob/main/scripts/role/gcr-rs-role.json) 

3. Record the **Access key ID** and **Secret access key**

4. In the Cloud9 terminal, config an AWS profile `rs-dev-workshop-cn` that can access China region (`cn-north-1`) 
```sh 
 aws configure --profile rs-dev-workshop-cn
```
![cn aws profile ](/images/cn-aws-profile.png)



