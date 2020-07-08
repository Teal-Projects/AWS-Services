h1. Description 

security group controls traffic to or from an EC2 instance according to a set of inbound and outbound rules.

h1. Main Features 
 

h5. General : 
* Security Groups are acting as a "firewall" on EC2 instances.
* They regulate :
** Access to Ports.
** Authorised IP range - IPv4 and IPv6.
** Control of inbound/outbound network (from other to the instance).
* A change in Security Group take effect imediately.
* You can not block specific IP addresses, you  have to use Network Access Control Lists.
* Can be attached to multiple instances, even across subnets.
* Locked down to a region/VPC.	
* You can create a Security group to authorize connection from an other Security Groups.
* AWS evaluates all rules for all the security groups associated with an instance before deciding whether to allow traffic in or out.
* The most permissive rule is applied.
* Security group rules are implicit deny, which means all traffic is denied unless an inbound or outbound rule explicitly allows it.
* Security groups are stateful; they automatically allow return traffic, no matter what rules are specified.

h1. Cost Strategies 

Free of charges.

h1. Service constrains 

h5. General :
* You can have 60 inbound and 60 outbound rules per security group.
