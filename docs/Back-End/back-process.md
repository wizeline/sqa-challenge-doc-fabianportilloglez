## **Introduction**

In this section is described the steps followed to complete the backend section of the SQA Onboarding challenge.
___
## **Prerequisites** *(optional)*
* Study or review about REST, API testing and Postman.
* Understand how **positive** and **negative** tests work and how should be their expected results.
___
## **Steps**

### **Postman**

1. Navigate to [**Todoist**](https://developer.todoist.com/rest/v1/#overview) API website:
   * Read the documentation to better understand the 'Todoist' REST API, HTTP requests methods, and expected responses for each case.
2. Download [**Postman**](https://www.postman.com/downloads)
3. Define a new collection and a new environment for your variables.
4. Create 2 folders: *Projects* and *Tasks* and define the folder/test structure you prefer *(this can change later in case you find a better structure)*.
5. Create your endpoints.
6. Think about your positive and negative scenarios you will test.
7. Define your variables and the test scripts for your endpoints.
8. Test your endpoints.
9. If everything goes well then run your collection using Postman until all tests passed. 
___
### **Newman**

1. Export your collections and environment variables and save them in a folder of your computer.
2. Install *newman* and *htmlextra* in your computer.
3. Open your terminal inside the folder you created and run your collection using newman and htmlextra to verify everything is working and the HTML reports with the results were created.
___
### **Jenkins**

1. Install Jenkins in your computer
2. Open your localhost in web browser and complete the steps for admin password, plugins and required.
3. Install plugins Manage Jenkins > Manage Plugins: *(HTML reporter, NodeJS, Blue Ocean, SonarScanner)*
4. Add NodeJs: Global Tools configuration > NodeJs > choose newman for npm.
5. Create a new item (job). Select 'pipeline' if you want to define a Jenkinsfile with different stages or environments, but if not then select 'freestyle project'.
6. Click on Configure:
7. In **Source Code Management** select git option and integrate your github repo, your branch and save your credentials.
8. In **Build environments** check the option of 'Provide Node & npm bin/ folder to PATH'
9. In **Build** add an 'Add build step' and create your command to install dependencies, HTML reports and run your collection and env variables from your github repo.
10. In Post-build Actions fill the fields. 
11. Exit 'configure' and click on **build now** to see if the job run fine and the HTML report with the results was generated.
12. In the case of Jenkinsfile, you define all the stages, sh commands and installation there.


    !!! note
        you can install and use Jenkins in your localhost or use a Docker image of Jenkins. Both are correct.
___

### **Sonarqube**

**Installation**:

1. I followed this [guide](https://medium.com/@lazyprogram/setup-sonarqube-on-mac-osx-c16a161d07d5)  to install and start Sonarqube in localhost with port 9000
2. I created a SonarScanner tool in Jenkins as shown in this [guide](https://igorski.co/sonarqube-scans-using-jenkins-declarative-pipelines/)
3. To configure [Sonarqube with jenkins](https://tomgregory.com/sonarqube-quality-gates-in-jenkins-build-pipeline/) I followed those steps, except for the Jenkinsfile sh commands, for that I followed [this](https://igorski.co/sonarqube-scans-using-jenkins-declarative-pipelines/) except for configuring *sonar-project.properties* file because for that I based on internet stuff and official documentation of Sonarqube.