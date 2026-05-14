---
title : "Clean up resources"
date: 2024-01-01
weight : 6
chapter : false
pre : " <b> 6. </b> "
---

### Terminate EC2 Instances

1. Terminate EC2 instance:
    - Access the Amazon EC2 console at [EC2](https://console.aws.amazon.com/ec2/).
    - On the left navigation bar, select "Instances."
    - Select all EC2 instances related to the lab.
    - Select **Instance state**.
    - Select **Terminate instance**.

   ![Terminate EC2](/images/6-ResourceCleanUp/001.png)

2. Confirm termination.

   ![Terminate EC2](/images/6-ResourceCleanUp/002.png)

3. Delete **Security Groups**
- Select **Security Groups**
- Select **Java Server SG**
- Select **Actions**
- Select **Delete security groups**

![Terminate EC2](/images/6-ResourceCleanUp/003.png)

4. Confirm delete

![Terminate EC2](/images/6-ResourceCleanUp/004.png)

