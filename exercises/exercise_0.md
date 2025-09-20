# Exercise 0

In this exercise, you get to familiarize yourself with Azure both theory and practical

## 0. Setup account

Make sure to setup an Azure account. If you are student in a school with Azure for students, you should go for this option. Otherwise you can create a free account.

## 1. Windows VM

Follow [these instructions in microsoft learn](https://learn.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal) to create a windows VM or [simply watch my video here](https://www.youtube.com/watch?v=4TgwLKhLoCc).

In my video I didn't show how to connect it with bastion, you should try to do it with bastion and see what happens. Navigate around in your VM a little bit and then delete the whole resource group to not incur any unneccessary costs.

## 2. Linux VM

Follow these [instructions here](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-portal?tabs=ubuntu) to create a Linux VM and try to SSH into it and create an nginx web server. Choose this VM size: `Standard B1s (1 vcpu, 1 GiB memory)`. SSH (secure shell) makes it possible for your local computer to connect to your VM.

You don't need to understand how nginx works. If you are finished and see the web server make sure to clean up the resources by deleting the resource group.

## 3. Theory questions

a) Can you explain these terms intuitively in an interview for cloud data engineer position?
- On-premises IT infrastructure
- Availability, uptime and downtime of an application
- Scalability of IT infrastructure

b) Suppose you have a MacBook and you want to spin up a Windows virtual machine to visit YouTube using the Chrome browser. What do you need to do?

- [ ] Find a secure physical room to store your Windows VM
- [ ] Create strong credentials for logging into your Window VM and keep the credentials securely
- [ ] Patch the Windows operating system regularly
- [ ] Install Google Chrome on the Windows VM
- [ ] Keep Chrome up to date (enable automatic updates)

c) Can you explain these concepts intuitively during an interview for cloud data engineer?

- What do we describe a containerized application as short-lived and stateless?
- Can a containerized application persistently store data?


d) Explain how vertical scaling contrasts against horizontal scaling

e) What are the differences between operational expenditure and capital expenditure?

f) What type of drawbacks are there with OpEx? 

g) How does Azure Static Web App work?



## Glossary

Fill in this table either by copying this into your own markdown file or copy it into a spreadsheet if you feel that is easier to work with.

| terminology                 | explanation |
| --------------------------- | ----------- |
| autoscaling                 |             |
| availability zone           |             |
| blob storage                |             |
| region                      |             |
| resource group              |             |
| role-based access control   |             |
| virtual machine             |             |
| virtual machine scale set   |             |
| virtual network             |             |
| app service                 |             |
| azure web app               |             |
| ssh                         |             |
| infrastructure              |             |
| infrastructure as code      |             |
| shared responsibility model |             |
| cloud provider              |             |
| cloud                       |             |
| cloud computing             |             |
| bastion                     |             |
| capital expenditure         |             |
| operational expenditure     |             |
| resource                    |             |
| resource group              |             |
| subscription                |             |
| data center                 |             |
| uptime                      |             |
| vertical scalability        |             |
| horizontal scalability      |             |
|                             |             |
