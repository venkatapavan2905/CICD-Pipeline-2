# Jenkins Pipeline for Java based application using Maven, SonarQube, Docker, Argo CD and Kubernetes

![Screenshot 2023-03-28 at 9 38 09 PM](https://user-images.githubusercontent.com/43399466/228301952-abc02ca2-9942-4a67-8293-f76647b6f9d8.png)


# Jenkins Pipeline Execution

![image](https://github.com/venkatapavan2905/CICD-Pipeline-2/assets/138016465/b39bbec0-3464-4fcc-8353-2270d4c7db36)


# Sonarqube Result

![image](https://github.com/venkatapavan2905/CICD-Pipeline-2/assets/138016465/f920aa9f-ef21-42a1-afc9-968882e4778f)


# Pods deployed in Argo CD 

![image](https://github.com/venkatapavan2905/CICD-Pipeline-2/assets/138016465/21e34db8-0b90-4ac7-99ba-fd446199a6d0)


# Access the Application Url using minikube service list

![image](https://github.com/venkatapavan2905/CICD-Pipeline-2/assets/138016465/55ca128e-4a96-4381-8b15-e9fe3fa5b729)

# Spring Boot App Service url from minikube cluster

![image](https://github.com/venkatapavan2905/CICD-Pipeline-2/assets/138016465/f94bb6e0-38ec-4c1c-942f-edd1dab2304b)


Here are the step-by-step details to set up an end-to-end Jenkins pipeline for a Java application using SonarQube, Argo CD and Kubernetes:

Prerequisites:

   -  Java application code hosted on a Git repository
   -  Jenkins server
   -  Kubernetes cluster
   -  Argo CD

Steps:

    1. Install the necessary Jenkins plugins:
       1.1 Git plugin
       1.2 Maven Integration plugin
       1.3 Pipeline plugin
       1.4 Docker Pipeline plugin
       1.5 Sonarqube scanner

    2. Create a new Jenkins pipeline:
       2.1 In Jenkins, create a new pipeline job and configure it with the Git repository URL for the Java application.
       2.2 Add a Jenkinsfile to the Git repository to define the pipeline stages.

    3. Define the pipeline stages:
        Stage 1: Checkout the source code from Git.
        Stage 2: Build the Java application using Maven.
        Stage 3: Run unit tests using JUnit.
        Stage 4: Run SonarQube analysis to check the code quality.
        Stage 5: Package the application into a JAR file.
        Stage 6: Promote the application to a production environment using Argo CD.

    4. Configure Jenkins pipeline stages:
        Stage 1: Use the Git plugin to check out the source code from the Git repository.
        Stage 2: Use the Maven Integration plugin to build the Java application.
        Stage 3: Use the SonarQube plugin to analyze the code quality of the Java application.
        Stage 4: Use the Maven Integration plugin to package the application into a JAR file.
        Stage 5: create a docker image from Dockerfile and push it to Docker hub.
        Stage 6: Use Argo CD to promote the application to a production environment.

    5. Set up Argo CD:
        Install Argo CD on the Kubernetes cluster.
        Set up a Git repository for Argo CD to track the changes in the Helm charts and Kubernetes manifests.

    6. Configure Jenkins pipeline to integrate with Argo CD:
       6.1 Add the manifests repo to Argo CD.
       6.2 update the deployments.yml for every new build using shell script in Update Deployment file stage in JenkinsFile.

    7. Run the Jenkins pipeline:
       7.1 Trigger the Jenkins pipeline to start the CI/CD process for the Java application.
       7.2 Monitor the pipeline stages and fix any issues that arise.

This end-to-end Jenkins pipeline will automate the entire CI/CD process for a Java application, from code checkout to production deployment, using popular tools like SonarQube, Argo CD and Kubernetes.
