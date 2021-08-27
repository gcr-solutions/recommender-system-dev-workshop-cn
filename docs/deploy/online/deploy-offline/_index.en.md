---
title: Deploy The Offline Logic
weight: 2
---

1. Setup offline

    ``` 
    cd /home/ec2-user/environment/recommender-system-dev-workshop-code/scripts
    ./setup-rs-system.sh deploy-offline
    ```

2. Go to [AWS code build console](https://console.aws.amazon.com/codesuite/codebuild/projects)
, check your code build projects, search `rs-dev-workshop-offline-`,  make sure all projects are built successful.

    ![Verify offline codebuild](/images/offline-code-build.png)

{{% notice info %}}
if some build projects show failed status, please retry
{{% /notice %}}

{{% notice info %}}
This will take about 5 ~ 10 minutes to provision
{{% /notice %}}







