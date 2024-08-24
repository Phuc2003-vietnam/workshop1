---
title: "Create auto scaling group"
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: " <b> 3.4 </b> "
---

- 1. From EC2 dashboard -> choose "Auto Scaling Groups" -> enter "ASG-workshop1" as name, choose "LT-ubuntu-with-application-NodeJS" as template and "Next"
![3tier](/images/3.test-HA-multi-server/015.png)

- 2. Choose "VPCWithOneServer" and select 2 subnets and "Next"
![3tier](/images/3.test-HA-multi-server/016.png)

- 3. Click "Attach to an existing load balancer", choose "TG-workshop1"
![3tier](/images/3.test-HA-multi-server/017.png)

- 3. Choose capacity like image, and "Target tracking scaling policy" with "Target value" of 20
![3tier](/images/3.test-HA-multi-server/019.png)
![3tier](/images/3.test-HA-multi-server/020.png)

- 4. Create Auto Scaling group and see the result
![3tier](/images/3.test-HA-multi-server/021.png)
![3tier](/images/3.test-HA-multi-server/022.png)
v