---
title : "HA-Scalable architecture"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 1.2 </b> "
---

### Definitions
* __High avability__: refers to the ability of a system or service to remain operational and accessible with minimal downtime. It is a key concept in systems design, especially for critical applications where uninterrupted service is crucial, e.g : banking, health care systems,...
* __Scalability__: design approach that allows a system to handle increasing loads or demands efficiently without compromising performance or reliability. It ensures that as the volume of data, traffic, or transactions grows, the system can expand to meet these demands seamlessly. 

### 3 tiers architecture

As the system grows, we often split it into tiers (also known as layers), which sets it on the path of greater scale and availability. Now every tier can be placed on its own box of the appropriate size and cost. We can choose bigger, better boxes with multiple levels of hardware redundancy for our database servers and cheaper, commodity-grade hardware for our web and application servers.

![3tier](/images/1.introduction/intro-3tier.png) 

### Adding redundancy server on webserver tier

The simplest way to increase system availability is by adding redundancy. Horizontal scaling, which involves adding more web servers to the web tier, is generally easier and more efficient than vertical scaling. By distributing the load across multiple servers, the likelihood of a complete failure decreases. This approach not only improves the availability of the web tier but also enhances the overall reliability of the entire system.

![3tier](/images/1.introduction/intro-webtier2server.png) 

Adding even one extra server to the web tier brings its availability by 8%. 

![3tier](/images/1.introduction/intro-webtier3server.png) 


As you can see , when having 3 webservers , it only enhances the performance 0.8% in comparision to have 2 webservers because the avaibility in same tier increase logarithmically

### Expand redundancy to other tiers

Let take another step and add more servers to our application server and master-slave DB where master DB is for write and slave DB is to be read from.

![3tier](/images/1.introduction/intro-last.png) 

The architecture now is tightly coupled , we have to reinvent the architecture for scalability

### Adding load balancer or message queue
As you can see from the above architecture, when adding, removing  new application server or somehow the server is down, we have manualy edit code on web server to connect or disconnect that application server, also the workload on each application server may not be equally distributed, affecting the system overall performance.

By implementing a load balancer, you can create a more robust and scalable architecture, capable of handling varying workloads efficiently.

![3tier](/images/1.introduction/intro-scaleable.png) 

One may ask: 
* "What about load balancer for Web Server?" : I think we can use DNS-based load balancing with round robin mechanism

* "If we only have 1 load balancer , can we consider it as single-point-failure architecture, as if load balancer is down , there is no way to forward request to application server": Great question ! We may use a standby load balancer in this scenario for high availability

*  "At any point of time, only one load balancer is serving all the requests. What if the number of incoming requests are too high?" : If the number requests is too high your will get timeouts and retry




