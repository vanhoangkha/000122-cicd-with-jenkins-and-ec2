---
title : "Set up Jenkins server"
date: 2024-01-01
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

## Prerequisite
We will run our Jenkins server using Docker, so a Docker environment is required:
- For MacOs/Window: install Docker Desktop.
- For Linux: install Docker.

## Set up
1. Paste command `docker run -d -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts` to your terminal
- **docker run**: Runs a Docker image. If the image is not available in local storage, it will be pulled from Docker Hub and run.
- **-d**: Runs the command in detached mode.
- **-p 8080:8080**: Maps Jenkins UI container's port to host's port.
- **jenkins/jenkins:lts**: Uses the latest Long-Term Support (LTS) Jenkins image.

Uses `docker ps` to list running container.

![Run Jenkins Image](/images/2-Preparation/2.1-SetUpJenkinsServer/001.png)

2. Logs Jenkins container and copy admin's password: `docker logs d338415bb43b`

![Get admin password](/images/2-Preparation/2.1-SetUpJenkinsServer/002.png)

3. Accesses to `localhost:8080` and paste the password copied in step 2, then click on **Continue** button

![Access Jenkins UI](/images/2-Preparation/2.1-SetUpJenkinsServer/003.png)

4. Clicks on **Install suggested plugins** and waits for all suggested plugins installed

![Install suggested plugins](/images/2-Preparation/2.1-SetUpJenkinsServer/004.png)
![Installing plugins](/images/2-Preparation/2.1-SetUpJenkinsServer/005.png)

5. After installation, you can either regist for an admin account (don't need to provide real info) and clicks on **Save and Continue** or just clicks on **Skip**. Then clicks on **Start using Jenkins**

![Regist Admin account](/images/2-Preparation/2.1-SetUpJenkinsServer/006.png)
![Start Using Jenkins](/images/2-Preparation/2.1-SetUpJenkinsServer/007.png)

