---
title: "DevOps for beginner day 1 blog"
datePublished: Mon Feb 17 2025 13:03:22 GMT+0000 (Coordinated Universal Time)
cuid: cm792gbaq002b09ihhcu42evr
slug: devops-for-beginner-day-1-blog
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1739796513327/62ff2e94-9ada-4227-a96d-7055ec899a8e.webp
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1739797343283/c9b222ff-bb7b-42cf-9545-89a7ebcceed7.webp
tags: devops, linux-for-beginners, 90daysofdevops

---

**Getting Started with DevOps: Learning Linux and Building a Password Generator**

The journey into DevOps often begins with mastering Linux, a fundamental skill for system administration, cloud computing, and automation. If you're new to DevOps, understanding the Linux command line, shell scripting, and basic server operations will set you on the right path. To solidify your learning, nothing beats hands-on experience, and a great beginner project is creating a password generator.

## **Why Linux is Essential for DevOps**

Linux is the backbone of modern cloud infrastructures and DevOps environments. Whether you're working with Docker, Kubernetes, or CI/CD pipelines, a strong grasp of Linux commands is invaluable. Here are some key areas beginners should focus on:

* **Basic Linux Commands**: `ls`, `cd`, `mkdir`, `rm`, `cp`, `mv`, `pwd`
    
* **User and File Permissions**: `chmod`, `chown`, `groups`
    
* **Process Management**: `ps`, `kill`, `top`, `htop`
    
* **Networking**: `ping`, `netstat`, `curl`, `wget`
    
* **Shell Scripting**: Automating tasks using Bash scripting
    

## **Your First DevOps Project: Creating a Password Generator**

### **Step 1: Writing the Script**

Open a terminal and create a new script file:

```bash
pass_gen.sh
```

```bash
#!/bin/bash

#simple Password Generator
echo"Welcome to Password Generator"

sleep 2

echo"Please Enter The Length Of The Password:-"
read PASS_LENGTH

for p in $(seq 1 );
do
   openssl rand -base64 48 | cut -c1-$PASS_LENGTH
done
```

### **Step 2: Making the Script Executable**

```bash
chmod +x pass_gen.sh
```

```bash
./pass_gen.sh
```

## Here the Cheatsheat of the Linux basic and advance commands

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1739798100803/df8e182a-5507-4178-ac93-e747d77a6986.png align="center")

[Here is my GitHub link](https://github.com/JibachhhMahto764/Devops-begginer-to-Advance/blob/main/Linux/linux_projects_1.sh).