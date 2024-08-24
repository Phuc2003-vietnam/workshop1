---
title: "Create target group"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 3.2 </b> "
---

- 1. From EC2 dashboard -> choose "Target Groups" -> choose "Create target group"
![3tier](/images/3.test-HA-multi-server/006.png)

- 2. Choose "Instances", enter "TG-workshop1" for name and Port "3000" and choose the VPC we create from cloudformation and click "Next"
![3tier](/images/3.test-HA-multi-server/007.png)
![3tier](/images/3.test-HA-multi-server/008.png)

- 3. Click the instance created from cloudformation and click "Include as pending below" then click "Create target group"
![3tier](/images/3.test-HA-multi-server/009.png)

