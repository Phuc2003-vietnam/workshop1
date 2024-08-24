---
title: "Testing"
date: "`r Sys.Date()`"
weight: 5
chapter: false
pre: " <b> 3.5 </b> "
---

- 1. Now you checkout the "LB-workshop1" with DNS name and config to loader.io as follow, remember to ssh to 1 of the server and change loader.txt. As you can see, we have 3 instance in the target group
![3tier](/images/3.test-HA-multi-server/027.png)
![3tier](/images/3.test-HA-multi-server/023.png)
![3tier](/images/3.test-HA-multi-server/024.png)
![3tier](/images/3.test-HA-multi-server/025.png)
![3tier](/images/3.test-HA-multi-server/026.png)

- 2. Config the test as follow, and you can see the result with 97 sucess request in comparision to 57 sucess in last test
![3tier](/images/3.test-HA-multi-server/028.png)
![3tier](/images/3.test-HA-multi-server/029.png)

- 3. When you enter the DNS name of load balancer, it uses round robin algorithm to route request to our instances in target group
![3tier](/images/3.test-HA-multi-server/030.png)
![3tier](/images/3.test-HA-multi-server/031.png)
![3tier](/images/3.test-HA-multi-server/032.png)
