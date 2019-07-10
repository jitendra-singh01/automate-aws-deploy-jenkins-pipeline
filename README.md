Jenkins is an open source automation server which helps to automate the non-human part of the software development process, with continuous integration and facilitating technical aspects of continuous delivery. It is a server-based system that runs in servlet containers such as Apache Tomcat. It supports version control tools like AccuRev, Subversion, Git, etc and can execute Apache Ant, Apache Maven and sbt based jobs as well as arbitrary shell scripts and Windows batch commands.

It industry uses the Jenkins in Automation testing & deployment with CI server facilitation. So we are trying to create Jenkins pipeline to do following processes:
1. Distributed testing on different slaves.
2. Grab all results of distributed testing.
3. Notify the team regarding results.
4. Call Jenkins job to execute AWS cloudformation to launch EC2 instance 
	a. Install Tomcat server
	b. Configure Tomcat server with user/password
5. Grab EC2 instance public IP address & pass as parameters to deployment job.
6. Call deployment job to depoly web application with help of Deploy to Container plugin.
7. Notify team by sending email with server URL.

Notes:
1. Pipeline script will notify team if testing is done successfully.
2. Pipeline script will notify team if testing is failed.
3. Pipeline script will notify team if deployment is done successfully or failed situation.
4. Jenkins jobs pull the code from github repositories.

Assets what repository contains:
1. Maven based Selenium testing code
2. Maven based demo web application
3. Cloudformation template to launch EC2 instance with Tomcat server installation.
4. Pipeline script which will all the tasks.
