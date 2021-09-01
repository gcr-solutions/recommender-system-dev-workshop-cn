---
title: Config AWS profile to access China region (Requirement For China Region)
weight: 7
---
## Create an AWS profile in Cloud9 to access China region

1. Go to **China region** AWS console [https://console.amazonaws.cn/iamv2/home?#/users](https://console.amazonaws.cn/iamv2/home?#/users)

2. Create an IAM user with [policy](https://github.com/gcr-solutions/recommender-system-dev-workshop-code/blob/main/scripts/role/gcr-rs-role.json) 

3. Record the **Access key ID** and **Secret access key**

4. In the Cloud9 terminal, config an AWS profile `rs-dev-workshop-cn`, set region: `cn-north-1`
```sh 
 aws configure --profile rs-dev-workshop-cn
```
![cn aws profile ](/images/cn-aws-profile.png)

5. Export the profile name as Env 
```sh
export CN_AWS_PROFILE=rs-dev-workshop-cn
echo "export CN_AWS_PROFILE=${CN_AWS_PROFILE}" | tee -a ~/.bash_profile
```

