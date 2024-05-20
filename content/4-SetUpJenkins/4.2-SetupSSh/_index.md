---
title : "Set up SSH"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

1. In **Dashboard**, selects **Manage Jenkins**, then selects **System**

![Navigate to System](/images/4-SetUpJenkins/4.2-SetupSSH/001.png)

2. Scrolls to Publish Over SSH, then selects **add** in **SSH Servers**

![Add SSH servers](/images/4-SetUpJenkins/4.2-SetupSSH/002.png)

3. Copy public IPv4 address of EC2 Instance

![Copy public IP](/images/4-SetUpJenkins/4.2-SetupSSH/003.png)

4. Use the public IP copied in step 3 to fill in information:
- **Name**: `Java Server 18.141.192.204` (Java Server + **Your IP**)
- **Hostname**: `ec2-18-141-192-204.ap-southeast-1.compute.amazonaws.com` (**Your Public IPv4 DNS**)
- **Username**: `ubuntu`
- **Remote Directory**: `/`

![Basic SSH Info](/images/4-SetUpJenkins/4.2-SetupSSH/004.png)

5. Copy private key **demo-jenkins-ec2.pem**

![Copy private key](/images/4-SetUpJenkins/4.2-SetupSSH/005.png)

6. Navigate back to Jenkins UI and fill in credential:
- Select **Advanced**
- Select **Use password authentication, or use a different key**
- **Key**: Enter **Your private key** (Copied from step 5)

![Configure credential](/images/4-SetUpJenkins/4.2-SetupSSH/006.png)

7. Test connection:
- Select **Test Configuration** to check connection result
- Select **Save**

![Test Connection](/images/4-SetUpJenkins/4.2-SetupSSH/007.png)


