h1. Description 

EC2 is a service that allows business subscribers to run application programs in the computing environment. The EC2 can serve as a practically unlimited set of virtual machines.

h1. Main Features 
 
h5. General : 
* Mainly consist in the capability of :
** Renting virtual machine (EC2).
** Storing Data on virtual drives (EBS).
** Dictributing load accress machines (ELB).
Scaling the services using an auto-scaling group (ASG).
* Termination Protection is turned off by default 
* The EBS root volume of the ANI can be encrypted 

h5. Creation Steps of an EC2 Instances : 
* Choose AMI 
* Choose the instances type 
* Configure instance 
* Add storage 
* Add Tags 
* Configure Security Group 
* Review  

h5. Metadata : 
* Used to get information about an instances. 
* curl http://<server_IP>/latest/meta-data/ 
* curl http://<server_IP>/latest/user-data/  

h1. Cost Strategies 
 
Please refer to Launch Types.

h1. Service constrains 


