---
title: "Testing"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 2.2 </b> "
---

- 1. Now you checkout the IPv4 of your newly-created EC2 , in my case that is 174.129.184.42
- 2. Access https://loader.io and config as following image, remember to enter your EC2 IPv4 at port 3000, in my case that is 174.129.184.42:3000 (port 3000 as your application run on this port).
![3tier](/images/2.test-HA-1server/003.png)
![3tier](/images/2.test-HA-1server/004.png)
- 3. SSH to your server and insert these commands (the image miss 2 last command)
##### sudo apt update
##### sudo apt install git npm nodejs
##### git clone  https://github.com/Phuc2003-vietnam/fcj-ha-architecture
##### cd fcj-ha-architecture
##### npm install express
##### echo <verification_token> > loader.txt => echo "loaderio-9a4748551499f812f4c74dbec54c5f4c5" > loader.txt
##### node index.js
![3tier](/images/2.test-HA-1server/005.png)
- 4. Click "verify" and enter configure the test to 100 clients in 1 Min and click "Run test"
![3tier](/images/2.test-HA-1server/006.png)
![3tier](/images/2.test-HA-1server/007.png)
- 5. The server is down due to memory leak while only serving 57 success request
![3tier](/images/2.test-HA-1server/008.png)
![3tier](/images/2.test-HA-1server/009.png)