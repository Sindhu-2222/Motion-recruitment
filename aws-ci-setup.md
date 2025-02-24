# Jenkins CI Pipeline Setup on AWS

This document provides step-by-step instructions to set up a Jenkins CI pipeline on AWS.

**Install Jenkins on AWS EC2
Step 1: Launch an EC2 Instance
- This is already written in the previous document 
Step 2: SSH into the EC2 Instance
- After that by using the ssh we are able to connect it with the local computer and after running that command we are connected with the server.
Step 3: Install Jenkins
- From the Jenkins Installing guide we have install Jenkins.
Step 4: Start Jenkins
-By continuing the installation guide the Jenkins is started.
**Initial Jenkins Setup
Step 1: Access Jenkins
- Open browser: `http://<your-ec2-public-dns>:8080`
Step 2: Unlock Jenkins
- Retrieve admin password from "sudo cat `/var/lib/jenkins/secrets/initialAdminPassword`"
Step 3: Install Suggested Plugins
Step 4: Create Admin User
**Configure Jenkins Job for CI Pipeline
Step 1: Create a New Jenkins Job
- Give any name for the New item
- Select pipeline and click 'ok'
Step 2: Configure Source Code Management (SCM)
- select the git
- give the Repo Url
- If got any error then goto tools and set the path of the git
- We will get the pipeline syntax set.
**Define Pipeline Stages
### Build Stage
### Test Stage
### Deploy Stage
-The above three stages script is written in the pipeline script and build is made success.
###Configure Build Triggers
### Additional Configuration
## Conclusion
This setup ensures a robust and automated CI pipeline using Jenkins on AWS.