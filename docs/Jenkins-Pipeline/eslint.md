**Optional installation plugins:**

        npm install eslint-plugin-prettier@latest --save-dev
___

        npm install eslint-plugin-only-warn --save-de
___ 
        npm install eslint@4.x babel-eslint@8 --save-dev
___
### **Steps**

[ESint doc](https://eslint.org/docs/user-guide/getting-started)

1. Install: 
        
        npm install eslint --save-dev

2. Init configuration file: 
   
        npm init @eslint/config

3. Define the configuration and rules. **example**:

        "rules": {
        "linebreak-style": [
            "error",
            "unix"
        ],
        "quotes": [
            "error",
            "single"
        ],
        "semi": [
            "error",
            "never"
        ]
   
4. Create a script in **package.json file** 
 
        "lint": "eslint ./src",

5. **run ESlint:**

**local:**

*example*

        eslint ./
//
        
        eslint ./ -o ./test/eslint-report.html

or 

        npm run lint

### **jenkinsfile**
        
        stage('Linting tools - Eslint') {
            steps {
                echo 'running Eslint..'
                sh 'npm run lint'
            }
        }    
___