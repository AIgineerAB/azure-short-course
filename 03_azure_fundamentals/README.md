# Fundamentals of Azure

**part 2 - theory**
<a href="https://youtu.be/eVBC8DiR8N0" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/azure/architecture.png?raw=true" alt="DESCRIPTION" width="600">
</a>

<br/>

**part 2 - portal practical**
<a href="https://youtu.be/4TgwLKhLoCc" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/azure/portal_practical.png?raw=true" alt="DESCRIPTION" width="600">
</a>


## How does Azure provide services? 
Whenever you create an Azure resource, you often have to choose a region for this resource. So what are region and related geogrphical terms in Azure? And why are they related to how Azure is working as a cloud platform?

### Datacenters
The physical infrastructure of Azure are housed in buildings called datacenters. These datacenters store physical computer servers together with networking, power and cooling facilities. These facilities are arranged in racks. These physical infrastructure are providing IT services to Azure customers over internet.

**Datacenter racks**

<img src="https://github.com/kokchun/assets/blob/main/azure/rack.png?raw=true" alt="data center rack" width="300">


### Regions
A region is a geographical area that is composed of one or multiple datacenters that are close to each others. When creating an Azure resource, we often need to choose from which region we would like the resource to be created. Then Azure internally assigns workloads across datacenters in the region to ensure balanced workloads. 

🔍 [Checkout the map of all Azure regions](https://datacenters.microsoft.com/globe/explore?info=region_swedencentral)

### Availability zones
Some regions are divided into availability zones. Each availability zone contains one or multiple datacenters. These availability zones are isolated with each others in the sense that when one goes down, another can continue working. This prevents downtime faced by customers.    

>[!Note]
>Choice of region for an Azure resource is affected by many factors such as:
>- latency- Azure servers respond to end-users closer to a region
>- your availability target- regions with availability zones gurantee uptime to end-users

## How can you provision an IT service on Azure?

### Resource groups and resources
All IT services you pay for in Azure are called **resources**: virtual machines, databases, networking setups are all separate resources. Azure requires you to create a **resource group** to group created resources. With a good structure of resource groups and resources, one can manage resources more efficiently as one can, for example, grant access for or delete all resources within a resource group altogether.

### Subscriptions
Before creating resource groups and resources, you need to first create a **subscription** under your **account**. You can create multiple subscriptions under your accounts. Then, you can start creating resource groups and resources under different subscriptions. 

Subscription serves as a unit of billing and administration. A good structure of subscription facilitates billing and other administration tasks. For instance, if a company is working with development and production environments, which means that there is an IT infrastructure supporting each environment, it can create DEV and PROD subscription to host resources used in each environment separately. There is no rule on how to organize your subscriptions. Some companies may want to create separate subscriptions for different departments like sales, IT, logistics departments etc.

🔍 [More details on the hierarchy of account -> subscription -> resource group -> resource](https://learn.microsoft.com/en-us/training/modules/describe-core-architectural-components-of-azure/6-describe-azure-management-infrastructure?ns-enrollment-type=learningpath&ns-enrollment-id=learn.wwl.azure-fundamentals-describe-azure-architecture-services)

>[!Tip]
>Follow exercise 0.1 to create a subscription and resource group to include a VM as a resource


## Examples of Azure resources
One can build an IT infrastructure with different Azure resources, or combine them with IT services on-premises or provided by other cloud platforms. Below are some Azure resources serving different purposes in an IT infrastructure:

>[!Note]
>There are much more Azure resources serving other purposes, like networking. These will not be covered here. 

### Computing
- Virtual machine (VM) <br> 
  VM works similarly as a physical computer. You configure specifications like OS, CPU and RAM etc upon creating a VM resource. It can be used as a lift-and-shift cloud migration as a company does not need to change its existing IT infrastructure much if it only wants to move physical servers to virtual ones. 
- Azure Web App <br> 
  After you have locally developed a web application, you can deploy it to Azure App Service. Azure App Service provides the underlying servers to host your production web application as an Azure Web App, which is reachable by end-users online.
- Azure Functions <br>
  It's cost efficient to deploy your codes to Azure Functions if you would only like to run your codes when certain events triggers. For example, if you receive an email etc. It avoids provisioning resources when there is no need. 
- Azure Container Instances <br> 
  Azure Container Instances are used to spin up containerized applications. This is suitable when you have containerized applications requiring different operation systems. 

🔍 [More on Azure compute services](https://learn.microsoft.com/en-us/training/modules/describe-azure-compute-networking-services/)

