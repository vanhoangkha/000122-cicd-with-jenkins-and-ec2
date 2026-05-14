---
title : "Config Security Group"
date: 2024-01-01
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

1. Accesses to AWS Console
2. Searchs for `Security Groups`, then choose **Security Group**

![Access Security Groups](/images/2-Preparation/2.2-ConfigSG/001.png)

3. Clicks on **Create security group**

![Click on SG](/images/2-Preparation/2.2-ConfigSG/002.png)

4. Configures Security Group
- **Security group name**: Enter `JavaServerSG`
- **Description**: Enter `Allows SSH for developers and 8080 port for users`
- **VPC**: choose **Default VPC**

![Input basic information](/images/2-Preparation/2.2-ConfigSG/003.png)

5. In **Inbound rules**:
- Select **Add rule**
- Select **Type**: SSH
- Select **Source**: Anywhere-IPv4
- Select **Add rule**
- Select **Type**: Custom TCP
- Select **Port**: 8080
- Select **Source**: Anywhere-IPv4

![Inbound rules](/images/2-Preparation/2.2-ConfigSG/004.png)

6. Checks **Outbound rules** and clicks on **Create security group**

![Outbound rules](/images/2-Preparation/2.2-ConfigSG/005.png)
