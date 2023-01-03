![[Pasted image 20221216133130.png]]
***
- ## Regions
	 Are geographic areas that host two or more availiability zones. 
	 So when you are building and choosing your custom services, you have opportunity to choose in what geographical region your infrastructure will be located.

	 It is very imortant to choose right region for your needs. Because in this way you can optimize latency while minimizing costs.

	 Also you have the opportunity to locate infostructure in the different regions at the same time. In case of different workload or distance from target customers.

***
- ## Availiability zones
	 Are collection of data centers within a specific region, each are isolated from one another but yet they are connected together by a fast, low-latencty link.

	 Benefit of having availiability zones isolated yet connected is fault tolerance.
	 When common points of failures occur, it doesn't affect all of your availiability zones because they are isolated.

	 How they are isolated?
	 Each availialbility zone is physically distinct, independent infrastructure.
	 Has their own discrete uninteruptable power supply, onsite backup generators, cooling equipment, network and connectivity.
 

***
- ## Edge locations
	 Host a content delivery network or CDN called [Amazone CloudFront].

	 [Amazone CloudFront] is used to deliver content to your customers. Requests for content are automatically routed to the nearest edge location so that the content is delivered faster to the end users.
	 
	 
