---
title: "Create elastic load balancer"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 3.3 </b> "
---

- 1. From EC2 dashboard -> choose "Load Balancers" -> choose "Create load balancer"
![3tier](/images/3.test-HA-multi-server/010.png)

- 2. Choose "Application Load Balancer"
![3tier](/images/3.test-HA-multi-server/011.png)
- 3. Enter name "LB-workshop1", choose "VPCWithOneServer" and choose 2 subnets, choose the existed Security group, forward to "TG-workshop1" and click create
![3tier](/images/3.test-HA-multi-server/012.png)
![3tier](/images/3.test-HA-multi-server/013.png)
![3tier](/images/3.test-HA-multi-server/014.png)

