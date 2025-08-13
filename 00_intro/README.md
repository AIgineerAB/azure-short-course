# Introduction to Cloud Computing with Azure

<a href="https://youtu.be/g-wRTFf6zuM" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/azure/intro_cloud.png?raw=true" alt="intro to cloud computing" width="600">
</a>

## On-premises vs cloud IT services

A company can hardly operate without various IT service components, which forms IT infrastructure of a company. Depending of the size of a company, the IT infrastructure can include various IT service components, and a data engineer can work with a smaller or larger part of the IT infrastructure. A data engineer should also understand basics of IT infrastructure as a datapipeline often involves integration of different components in a company's IT infrastructure.

Let's have a look at a simple example of a small e-commerce company. This company is selling clothes online and gather data such as warehouse stock levels, product prices and customer data etc from external data sources.

The company is renting a physical office. In one floor, it places two desktop computers to host the database server and web server. This floor needs physical security measures to prevent unauthorized access, and also air-conditioning to avoid overheat of the servers. This company employs a database administrator to manage the DB server and a web developer to develop its website. They work with laptops.

These laptops are connected to the two servers in a Local Area Network (LAN) so that these computers can communicate with each others. Apart from the LAN, additional networking setups are needed so that the DB server can receive inbound traffic from external data sources and consumers can access the website for online shopping.

The computers (hardware), applications for DB and web development installed on the computers (software), and networking devices connecting themselves and to the outside world form a simple example of IT infrastructure of this type of business.

  <img src="https://github.com/kokchun/assets/blob/main/azure/onprem_it.png?raw=true" alt="on premise IT" width="500">

## Why do we need cloud platform?

The on-premises IT infrastructure above requires an upfront cost to set up different computers and networking devices for the company to start operate. At the same time, the capacity of the two servers are relatively fixed and the company cannot react to varying inflow of data or customers browing its website. This results in downtimes as the company cannot scale up its IT infrastructure flexibly. These issues prompt companies to migrate to cloud IT infrastructure.

> [!Note]
> Cloud IT infrastructure is the delivery of IT services OVER THE INTERNET so that a company does not need to maintain physical hardwares and premisese as before

For example, the company can alternatively set up a cloud IT infrastructure as below. Instead of purchasing two server computers and placing them in a physical office, it can use cloud DB and web servers and pay for the actual usage of the servers. The DBA and web developer can connect to these cloud servers via internet. The benefits are:

- **cost efficiency** <br>
  the company now does not need to pay for the upfront cost to purchase the server computers, and extra cost to arrange a secure physical office to accomodate them.
- **scalability and availability** <br>
  cloud providers maintain many server computers behind the scenes and are able to scale up their IT services flexibly. In this case, the capacity of the cloud and web servers can be adjusted according to realtime needs. Downtimes of the company's website can thus be prevented, without the company purchasing more capable computers that are left idle during off-peak hours when less customers are browsing the website.


<img src="https://github.com/kokchun/assets/blob/main/azure/cloud_it.png?raw=true" alt="IT infrastructure on the cloud" width="500">

## Other videos 📹

## Read more 👓
