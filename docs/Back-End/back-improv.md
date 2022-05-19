### **Docker**

* Instead of having the configuration just installed in computer, could be used Docker for pull some Jenkins image from Docker hub, having the service running in a container and also having a Dockerfile and volumes for data persistence.

* Also Docker could be useful for isolate the work, integrate with other tools and for fast/easy configuration just to mention some advantages.

### **Jenkins & Jenkinsfile:**
* For next time can be nice taking more time to add more clean commands and scripts in Jenkinsfile
* Also include better practices with Jenkins like save some information in environment variables and just call them.

### **API documentation.**
Postman API documentation is cool but maybe in future can be considered Swagger.

### **Postman:**
* **BDD:**
  * Organize the tests using BDD('Describe') 
  * **BDD Hooks:**
    * Use before, after, beforeEach, and afterEach hooks to reuse code and tests
  * **Automatic Error Handling:**
    * If a script error occurs, only that one test fails. Other tests still run.
  * Nested describe blocks:
    * You can nest describe blocks to logically group your tests
* **Mock servers:**
  * Mock some difficult response like xx500 responses or other scenarios.
* **Monitor**
  * Monitor the collection to schedule some days and times to run automatically and receive the response in your email.
* **Improve the tests:**
  * In some tests could be improved the way that variables are defined and then used. 
  * randomData can also be defined to use in POST requests.
