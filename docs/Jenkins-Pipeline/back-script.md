### **Steps**
Prerequisites: 
Install plugin to generate reports using newman.

        npm install -g newman-reporter-htmlextra

1. Create a script in **package.json file** 
 
            "backendTests": "newman run ./src/backend/postman/todoist-backend.postman_collection.json -e ./src/backend/postman/todoist-backend.postman_environment.json -r htmlextra --reporter-htmlextra-export ./report_results/test_results_report.html"

2. **run backend scripts:**

**local:**

*example*

        npm run backendTests

**jenkinsfile**
        
        stage('Backend') {
            steps {
                echo 'running backend tests...'
                sh 'npm run backendTests'
            }
        } 
___