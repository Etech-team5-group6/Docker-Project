# Docker-Project


1.	What is docker? - Francis





2.	List 3 differences between a docker container and virtual machine - Francis





3.	Why do companies prefer microservice over monolith applications? - Francis





4.	What is a docker image? - Francis





5.	What is a docker container? 

    A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run     an application: code, runtime, system tools, system libraries and settings.





6.	How do you troubleshoot miscommunications of docker containers? - Nelly





7.	How are you using docker in your current role at Etech Consulting? - Nelly




8.	What implementation will you deploy to ensure data is persisted from a docker container 
application? - Nelly





9.	What plugin can you use to integrate Jenkins to docker APIs? - Aubin




10.	Write down the process to delete a docker image that is currently running an application - Aubin





11.	What will you do if your docker image was wrongly created? - Aubin



Part2: 
Write down your CICD pipeline workflow from developer environment till creating your docker image and backing up the docker image to a container registry of your choice. 

  At Etech Consulting it is a standard that each developer must install the talisman tools in their environment which ensure that whenever they try to make a commit it is going to check and make sure that they are not committing any vulnerable information into the code so that we can have clean code for our deployment. Once developer push there code into GitHub, (where we maintained a minimum of 3 branches feature, staging and main branches at the end code at the feature branches will be deploy to the dev environment, code in the staging branch will be deploy to the staging environment and code in the main branch will be deploy to the production) when developer commit their code into GitHub, and  they create a pull request Jenkins is going to pull the code on the branch where the pull request is created  and is going to deploy an application into our dev Environment. After everything is done the code is going to be move from the staging branch to the main branch.
 From the main branch where we are creating a change in our application Jenkins is going to pull those code then integrate with maven using plugins. Maven then is going to use the project object model .XML file definition which count down with the clone of the repository. Jenkins is going to build our artifact then connect to SonarQube using sonar- sonar plugging. Once it is connected to SonarQube it run quality code analysis. 
  At Etech consulting we define high level parameter like code coverage, code smell, vulnerability, duplicate line to make sure that the code we use to deploy our application are free of bug, free from vulnerabilities. Once the SonarQube code analysis is done, Jenkins is going to integrate with nexus using the nexus artifact uploader plugging it is going to back up those artifacts into a release repository in nexus. Once Jenkins backup the artifact into nexus, it is going to connect with Docker. With Docker file that came with the repository, Jenkins is going to build our Docker image. Because we are deploying microservices Jenkins is going to build our docker image. Once Jenkins build our Docker image, Jenkins is going to backup those images into our Elastic container private registry in AWS.


(Hints: diagrams are also accepted include the explanations) 

![image](https://user-images.githubusercontent.com/127711433/236641484-ed8c6431-40c1-4984-8ea9-1b47735c0e16.png)
