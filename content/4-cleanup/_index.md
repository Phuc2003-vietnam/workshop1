+++
title = "Clean up resources"
date = 2022
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

We will take the following steps to delete the resources we created in this exercise.

#### Remove Auto Scaling Group:

   + Access EC2 Management Console
   + On the left navigation bar, select Auto Scaling Groups
   + Select Auto Scaling Group related to the lab.
   + Click Delete

#### Remove Load Balancer

   + Access EC2 Management Console
   + On the left navigation bar, select Load Balancers
   + Select Load Balancers related to the lab.
   + Click Actions
   + Click Delete

#### Remove Target Group

   + Access EC2 Management Console
   + On the left navigation bar, select Target Groups
   + Select Target Groups related to the lab.
   + Click Actions
   + Click Delete

#### Delete Launch Template

   + Access EC2 Management Console
   + On the left navigation bar, select Launch Template:
   + Select Launch Template related to the lab.
   + Click Actions
   + Click Delete template

#### Delete Stack

   + Access Cloudformation console
   + Select the stack you created
   + Click Delete 