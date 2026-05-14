---
title : "Create Free Style Job"
date: 2024-01-01
weight : 4
chapter : false
pre : " <b> 4.3 </b> "
---

1. Navigates to **Dashboard**, then selects **New Item**

![Select New Item](/images/4-SetUpJenkins/4.3-CreateFreeStyleJob/001.png)

2. Enters `workshop1`, selects **Freestyle project**, then selects **OK**

![Create new item](/images/4-SetUpJenkins/4.3-CreateFreeStyleJob/002.png)

3. Configures Source Code Management
- Select **Source Code Management**
- Select **Git**
- **Repository URL**: `https://github.com/MQuang200/SimpleJavaProject.git` (This is my public repository for this demo)
- **Branch Specifier**: Enter `*/FCJ-workshop1`

![Config SCM](/images/4-SetUpJenkins/4.3-CreateFreeStyleJob/003.png)

4. Configures clean step:
- Select **Build Steps**
- Select **Add build step**
- Select **Invoke Gradle Script**

![Add clean step](/images/4-SetUpJenkins/4.3-CreateFreeStyleJob/004.png)

- **Gradle Version**: Select **gradle 8.6**
- **Tasks**: Enter `clean`

![Add clean step](/images/4-SetUpJenkins/4.3-CreateFreeStyleJob/005.png)

5. Configures clean step:
- Select **Build Steps**
- Select **Add build step**
- Select **Invoke Gradle Script**

![Add build step](/images/4-SetUpJenkins/4.3-CreateFreeStyleJob/004.png)

- **Gradle Version**: Select **gradle 8.6**
- **Tasks**: Enter `build`

![Add build step](/images/4-SetUpJenkins/4.3-CreateFreeStyleJob/005.png)

6. Configures clean step:
- Select **Build Steps**
- Select **Add build step**
- Select **Invoke Gradle Script**

![Add test step](/images/4-SetUpJenkins/4.3-CreateFreeStyleJob/006.png)

- **Gradle Version**: Select **gradle 8.6**
- **Tasks**: Enter `test`

![Add test step](/images/4-SetUpJenkins/4.3-CreateFreeStyleJob/007.png)

7. Configures deploy step:
- Selects **Post-build Actions**
- Selects **Add post-build action**
- Select **Send build artifacts over SSH**

![Add deploy step](/images/4-SetUpJenkins/4.3-CreateFreeStyleJob/008.png)

- **Name**: Select **Java Server 18.141.192.204** (Java Server + **Your IP**)
- **Source files**: Enter `build/libs/demo-0.0.1-SNAPSHOT.jar`
> Base on build.gradle file in my project, **demo-0.0.1-SNAPSHOT.jar** will be built and placed in **build/libs** directory after **build step**
- **Remove prefix**: Enter `build/libs`
> We only want to send artifact file to server
- **Remote directory**: Enter `/home/ubuntu`
> Directory in server where Jenkins sends artifact to
- **Exec command**: Enter `screen -dmS demo java -jar demo-0.0.1-SNAPSHOT.jar`
> Deploy Java Springboot jar file and attached process to a screen

![Add deploy step](/images/4-SetUpJenkins/4.3-CreateFreeStyleJob/009.png)


