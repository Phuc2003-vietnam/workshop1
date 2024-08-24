---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
In early days, developers deployed their application by keeping everything on a single box (or a single EC2 instance if I were to do it in the cloud) as it seems to be the easiest way. The main issues with this approach are of course scale and availability. You can only support as many customers as your single box and should this single box fail, you won’t support any at all. And while these may not be your primary concerns in the early stages, as your system matures and your customer base grows, availability and scale will become more important.

![3tier](/images/1.introduction/intro-3architectures.jpg) 


### Content
  - [Little exercise before jump into](1.1-theProblem/_index.md)
  - [HA-Scalable architecture](1.2-HA-scalable-architecture/_index.md)