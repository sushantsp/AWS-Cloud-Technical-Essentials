# what are Regions ?

Regions are geographic locations worldwide where AWS hosts its data centers. AWS Regions are named after the location where they reside. For example, in the United States, there is a Region in Northern Virginia called the Northern Virginia Region and a Region in Oregon called the Oregon Region. There are Regions in Asia Pacific, Canada, Europe, the Middle East, and South America, and AWS continues to expand to meet the needs of its customers.Each AWS Region is associated with a geographical name and a Region code.

![alt text](.images/Regions.png)


AWS Regions are independent from one another. This means that your data is not replicated from one Region to another, without your explicit consent and authorization.

* Prices, Latencey, Data Compliance and Service Availibility are some of the areas one should look at before choosing a region


# Availibility Zone


Inside every Region is a cluster of Availability Zones (AZ). An AZ consists of one or more data centers with redundant power, networking, and connectivity. These data centers operate in discrete facilities with undisclosed locations. They are connected using redundant high-speed and low-latency links.AZs also have a code name. Since they’re located inside Regions, they can be addressed by appending a letter to the end of the Region code name. For example:

* us-east-1a: an AZ in us-east-1 (Northern Virginia Region)

* sa-east-1b: an AZ in sa-east-1 (São Paulo Region in South America)

If you see that a resource exists in us-east-1c, you know this resource is located in AZ c of the us-east-1 Region.


# SCOPE AWS Services

Region scoped services - you only need to select the Region you want to use. If you are not ased about az while selecting a service that means that service is Region Scoped. Or that service operates on Region Scope level. For region-scoped services, AWS automatically performs actions to increase data durability and availability. 
- On the other hand, some services ask you to specify an AZ. With these services, you are often responsible for increasing the data durability and high availability of these resources. 
- To keep your application available, you need to maintain high availability and resiliency. A well-known best practice for cloud architecture is to use Region-scoped, managed services. These services come with availability and resiliency built in.When that is not possible, make sure the workload is replicated across multiple AZs. At a minimum, you should use two AZs. If one entire AZ fails, your application will have infrastructure up and running in at least a second AZ to take over the traffic.
