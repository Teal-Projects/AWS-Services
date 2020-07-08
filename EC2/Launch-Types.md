h1. Description 

EC2 is a service that allows business subscribers to run application programs in the computing environment. The EC2 can serve as a practically unlimited set of virtual machines.

h1. Main Features 
 
h5. On-Demand :
* Pay for compute capacity by the hour or the second depending on which instances you run.
* Highest cost.
* Recommended for :
** Users that prefer the low cost and flexibility of Amazon EC2 without any up-front payment or long-term commitment
** Applications with short-term, spiky, or unpredictable workloads that cannot be interrupted
** Applications being developed or tested on Amazon EC2 for the first time.

h5. Reserved Instances :
* Provide you with a significant discount (up to 75%) compared to On-Demand instance pricing. In addition, when Reserved Instances are assigned to a specific Availability Zone, they provide a capacity reservation, giving you additional confidence in your ability to launch instances when you need them.
* Reserved for 1 or 3 years.
* Reserved a specific instances type.
* Recommended for :
** Applications with steady state usage, like databese.
** Applications that may require reserved capacity.
** Customers that can commit to using EC2 over a 1 or 3 year term to reduce their total computing costs.
* Convertible Reseved Instances :
** Can change the EC2 instance type.
** Up to 54% discount.
* Scheduled Reserved Instances :
** Launch within time window you reserve.
** When you require a fraction of day/week/month.

h5. Spot instances :
* Allow you to request spare Amazon EC2 computing capacity for up to 90% off the On-Demand price.
* Instances that you can "lose" at any point of time if your max price is less than the current spot price.
* Spot Instance Request :
** Define max spot price and get the instance while current spot price < max.
*** The hourly spot price varies based on offer and capacity.
*** If the current spot price > your max price you can choose to stop or terminate your instance with a 2 minute grace period.
** Spot Block
***"Block" spot instance during a specified time frame (a to 6 hours) without interruptions.


* Recommended for :
** Applications that have flexible start and end times (Batch job, Data analysis,image processing...).
** Applications that are only feasible at very low compute prices.
** Users with urgent computing needs for large amounts of additional capacity.
* Great combo : Reserved Instances for baseline + On-Demand & Spot for peaks.

h5. Dedicated Hosts :
* a physical EC2 server dedicated for your use. Dedicated Hosts can help you reduce costs by allowing you to use your existing server-bound software licenses, including Windows Server, SQL Server, and SUSE Linux Enterprise Server (subject to your license terms), and can also help you meet compliance requirements.
* Full control of EC2 Instance placement.
* Allocated for your account for a 3 year period reservation.
* More expensive.
* Can be purchased On-Demand (hourly).
* Can be purchased as a Reservation for up to 70% off the On-Demand price.
* Recomanded for :
** Software who have complicated licensing model.
** Companies that have strong regulatory or compliance needs.

h5. Dedicated Instances :
* Instances running on hardware that's dedicated to you.
* May share hardware with other instances in same account.
* No control over instance placement (can move hardware after Stop/Start).

h5. Which host is right for me (Example with hotel booking) :
* On demand :
** Coming and staying in resort whenever we like, we pay the full price.
* Reserved :
** Like planning ahead and if we plan to stay for a long time, we may get a good discount.
* Spot instances :
** The hotel allows people to bid for the empty rooms and highest bidder keeps the rooms. You can get kicked out at any time.
* Dedicated Hosts :
** We book an entire building of the resort.

h1. Service constrains 


