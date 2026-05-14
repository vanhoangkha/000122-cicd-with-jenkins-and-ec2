---
title : "Install Tools"
date: 2024-01-01
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

### Install necessary tools for Java server

1. Accesses the **AWS Management Console** interface:
- Navigates to EC2
- Chooses **EC2**
- Chooses **Instances**
- Selects **Java Server**
- Clicks on **Connect**

![Navigate to EC2](/images/3-CreateEC2/3.2-InstallTools/001.png)
![Navigate to EC@](/images/3-CreateEC2/3.2-InstallTools/002.png)

2. Chooses SSH type:
- Selects EC2 Instance Connect
- Clicks on **Connect**

![Choose SSH type](/images/3-CreateEC2/3.2-InstallTools/003.png)

3. In **EC2 Instance Connect**, paste command to console `sudo apt update && sudo apt install openjdk-17-jre-headless -y && sudo apt install net-tools -y`
- Install Java 17 for running Java Springboot project
- Install net-tools for network troubleshoot

![Choose SSH type](/images/3-CreateEC2/3.2-InstallTools/004.png)

