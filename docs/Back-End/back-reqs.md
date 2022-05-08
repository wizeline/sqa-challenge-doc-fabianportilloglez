## **Backend project**

1. Navigate to Todoist API
2. Download Postman
    1. Define a new collection and a new environment for your variables
   
### **Backend Automation Tasks:**
1. Get your authorization token and save it as an environment variable
2. Create a new folder inside your collection for projects and another one for tasks.
3. Create the following endpoints and its corresponding Tests: *status codes, content, json schema,response time, etc.*

**a) Projects**

1. Get all projects
2. Create a new project
3. Get a project
4. Update a project
5. Delete a project

**b) Tasks:**

1. Get active tasks
2. Create a new task
3. Get an active task
4. Update a task
5. Close a task
6. Reopen a task
7. Delete a task
8. Create Negative scenarios for each endpoint

    !!! info 
        Integrate one framework for API Test Automation i.e. *Newman *Axios *SuperTest *chai-http So you can run your tests from the command line
