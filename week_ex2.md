## Market status

[Reference](https://www.datamation.com/cloud-computing/cloud-computing-companies.html)

###### AWS
* Market leader
* Theme was making everything easier for customer
* Most popular for strategic, organization-wide adoption
* Wide scope of services ranging from analytics to database and robotics

###### Microsoft Azure
* Compatible with the .NET programming language and is integrated with Visual Studio
* Favorite among .NET developers because of this
* Enterprise-class is given

###### IBM Cloud
* Has long history and offerings from different times of cloud evolution which makes IBM top choice for legacy systems

###### Google Cloud
* Main theme is AI and making it accessible & discussing AI ethics
* Strongest AI results
* Market rate grows linearly

###### Alibaba Cloud
* Lead provider in China
* Aggressive plans on cloud business

###### Oracle Cloud
* Differs from other top players with enterprise focus, deep pockets and general digitization of everything

Alibaba will probably gain more market share during 2019 as it's revenue doubled on 2018. AWS is remarkably larger than the others and also most used in APAC area so I think it will keep it's position as the top dog in the game. Google's main focus is on AI which takes it's toll on cloud services. IBM and Azure have their own niche customers as long as their service is needed.

## AWS Security Best Practices Whitepaper

* Customer (me) is responsible for secure operating systems, platforms and data

1. Prioritize
	* Before doing anything with AWS controls and tools, a security strategy should come first. It makes continuous developing and deployment more safe and easier.

2. Logs
	* Collect logs on what is happening on a host or workload

3. HIDS
	* Host-based intrusion detection (knowledge of what, when, where, before, during and after attack).
	* Accounts to intrusions that are not trackable in log files

4. Liabilities
	* It is important who is responsible in case of intrusion. 
	* Also advance knowledge possible of liabilities is important 

5. Responsibility
	* I, as a customer, should know where AWS tools and configurations responsibilities end and mine begin.
	* Customer should work with cloud service providers in parallel to ensure compliance

6. Protect and monitor credentials
	* AWS security is difficult to breach by itself and attacks against cloud server providers are fairly uncommon
	* It is important to monitor and secure credentials with e.g. multi factor authentication, monitoring anomalous logins, logging service, and credential rotation

7. Securing data
	* Protecting data at rest and at transit
	* Communication over public links makes data transit risky so network traffic should be protected

## IAM (Identity and Access Management) Roles on EC2

[Reference](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements.html)

An IAM role lets one define a set of permissions to access the resources that a user or service ( in this case, the script ) needs without attaching the role to a specific IAM user.

I would create an identity policy for the script. In JSON policy element, in the Action element, I'd specify that the script can start an ec2 instance and check the status. In NotResource element I'd list out all the instances that security team use so that the script can't access them.	