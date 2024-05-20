---
title : "Create EC2"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---

1. Access the **AWS Management Console** interface:
- Navigate to EC2
- Choose **EC2**

![Create EC2](/images/3-CreateEC2/3.1-CreateEC2/001.png)

2. Within the **EC2** interface:
   - Select **Instance**
   - Click on **Launch instances**

![Create EC2](/images/3-CreateEC2/3.1-CreateEC2/002.png)

3. Provide a Name and tags for the instance, enter `Java Server`:

![Create EC2](/images/3-CreateEC2/3.1-CreateEC2/003.png)

4. Choose the **Application and OS Images (Amazon Machine Image**
- Select **Quick Start**
- Choose **Ubuntu**
- Select an **AMI**

![Create EC2](/images/3-CreateEC2/3.1-CreateEC2/004.png)
<!-- ::: warning Important Note -->
<!-- For the **Tenancy** configuration, it's recommended to keep the default setting. Switching to **Dedicated** may restrict the creation of certain **EC2 Instance types** within the VPC, as they require the default tenancy. -->
<!-- ::: -->

5. Select an **Instance type** and opt to **Create a new key pair**

![Create EC2](/images/3-CreateEC2/3.1-CreateEC2/005.png)

6. In the **Create key pair** interface:
- Specify the **Key pair name**, e.g., **```demo-jenkins-ec2```** (optional name, you can set any).
- Choose **Key pair type: RSA**
- Select **Private key file format: .pem**

![Create EC2](/images/3-CreateEC2/3.1-CreateEC2/006.png)

7. Configure the **Network**:
- For **Firewall (Security Group)**, select **Select existing security group**
- Choose **JavaServerSG**
- Click **Launch instance**

![Create EC2](/images/3-CreateEC2/3.1-CreateEC2/007.png)

8. Complete the instance creation

![Create EC2](/images/3-CreateEC2/3.1-CreateEC2/008.png)

9. Wait for about 5 minutes until the **Status check** shows **2/2 checks passed**

![Create EC2](/images/3-CreateEC2/3.1-CreateEC2/009.png)

