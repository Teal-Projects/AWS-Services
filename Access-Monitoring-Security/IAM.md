h1. Description 

AWS IAM is generally defined as the Identity and Access Management, which is derived as one of the best web services that help to provide the secured control access to all the AWS resources. You can use this IAM option in order to control both authorized and unauthorized resources easily.

h1. Main Features 
 

h5. General : 
* IAM has a global view.
* Centralised control of your AWS account 
* Policies are JSON document to control permission
* Root account should never be used (except for initial setup.) and shared
* Shared Access to your AWS Account 
* Granular Permissions 
* Multifactor Authentication 
* Provides temporary access for users/devices and services 
* allow setep Password policies 
* Integration AWS services 
* PCI DSS Compliance 
* New users get an Access key ID and secret key 

h5. Components :
* Users
** Usually a physical person.
* Group
** Can be : Functions (admins, devops...), Team (Engineering, design...), Contains users!
* Roles (Allowing one part of aws to do an other part).
** Internal usage within AWS resources.
** Roles are much more easier to manage than the access and secret keys
** Roles can be assigned to EC2 instances after it is created.
** Roles are universal, you can use it in any region.

h5. IAM Federation :
* Bug entreprise usually integrate their own repository of users with IAM.
* This way, one can login into AWS using their company credentials.
* Identity Federation uses the SAML standard (Active Directory)

h5. RAM
* Resource Access Manager. Allows resources sharing between accounts.
* Ressources that can be share : 
** App Mesh, Aurora, CodeBuild, EC2, EC2 Image Builder, License Manager, Resource Groups, Route 53 

h1. Cost Strategies 

IAM roles are free of charge.

h1. Service constrains 
 
