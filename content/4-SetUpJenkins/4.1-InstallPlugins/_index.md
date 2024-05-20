---
title : "Install and Configure Plugins"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

### Installs **Publish Over SSH** plugins
1. Opens web browser and accesses `localhost:8080`, then selects **Manage Jenkins**

![Access Jenkins UI](/images/4-SetUpJenkins/4.1-InstallPlugins/001.png)

2. Selects **Plugins**

![Select Plugins](/images/4-SetUpJenkins/4.1-InstallPlugins/002.png)

3. Installs **Publish Over SSH plugin**:
- Select **Available Plugins**
- Search **SSH**
- Choose **Publish Over SSH** plugin
- Select **Install**

![Install Plugins](/images/4-SetUpJenkins/4.1-InstallPlugins/003.png)

4. Waits for installation and navigates back to **Dashboard**

![Nagigate back](/images/4-SetUpJenkins/4.1-InstallPlugins/004.png)

### Configures **Gradle 8.6**
1. In **Dashboard**, selects **Manage Jenkins**, then selects **Tools**

![Navigate to Tools](/images/4-SetUpJenkins/4.1-InstallPlugins/005.png)

2. Configures **Gradle 8.6** for Package Manager
- Scrolls to **Gradle Installation**
- Chooses **Add gradle**
- **name**: Enter `gradle 8.6`
- **Version**: Select **Gradle 8.6**
- Select **Save**

![Configure gradle 8.6](/images/4-SetUpJenkins/4.1-InstallPlugins/006.png)
