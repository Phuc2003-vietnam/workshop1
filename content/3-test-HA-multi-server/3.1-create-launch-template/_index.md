---
title: "Create launch template"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 3.1 </b> "
---

- 1. From EC2 dashboard -> choose Instances -> choose the newly-created EC2 instance -> then we creat the launch template from this instance 
![3tier](/images/3.test-HA-multi-server/001.png)

- 2. Enter "Launch template name" : " LT-ubuntu-with-application-NodeJS"
![3tier](/images/3.test-HA-multi-server/002.png)

- 3. In "Subnet", choose "Don't include in launch template", and choose the existed security group created from cloudformation
![3tier](/images/3.test-HA-multi-server/003.png)

- 4. Enter the code into "User data" and click "Create launch template" . It will automatically run these commands when an EC2 instance is created.

```html
#!/bin/bash

# Update the package list and install required packages
sudo apt update

sudo apt install -y git npm nodejs

# Clone the repository
git clone https://github.com/Phuc2003-vietnam/fcj-ha-architecture

# Change directory to the cloned repository
cd fcj-ha-architecture

# Install the necessary npm packages
npm install express

# Run the Node.js application
node index.js
```

![3tier](/images/3.test-HA-multi-server/004.png)

- 5. The successs response

![3tier](/images/3.test-HA-multi-server/005.png)
