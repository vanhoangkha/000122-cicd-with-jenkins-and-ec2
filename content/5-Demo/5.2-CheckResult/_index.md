---
title : "Check result"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 5.2 </b> "
---

1. Navigate back to **EC2 Instance Connect**
2. Paste command `ps -aux | grep java` to check for java process

![Check java process](/images/5-Demo/5.2-CheckResult/001.png)

3. Paste command `netstat -lnpt` to check for port using in server

![Check java process](/images/5-Demo/5.2-CheckResult/002.png)

4. Visit `http://18.141.192.204:8080/` to access to webpage

![Check java process](/images/5-Demo/5.2-CheckResult/003.png)

