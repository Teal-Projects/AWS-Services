h1. Description 

When you hibernate an instance, we signal the operating system to perform hibernation (suspend-to-disk). Hibernation saves the contents from the instance memory (RAM) to your Amazon EBS root volume.

h1. Main Features 
 
h5. General :
* The in-memory (RAM) state is preserved
* The instance boot is much faster !
* Under the hood: the RAM state is written to a file in the root EBS volume.
* The root EBS volume must be encrypted.

h5. Use cases :
* Long-running processing
* Saving the RAM state.
* Services that take time to initialize.

h1. Cost Strategies 
 

h1. Service constrains 
 
h5. General :
* Does not support all family instances.
* The RAM size must be < 150 GB.
* Does not suport bare metal instances.
* The root volume must be EBS, encrypted, and large to contain a dump of the RAM.
* Available for On-Demand and Reserved Instances.
* Can not hibernate for more than 60 days.
