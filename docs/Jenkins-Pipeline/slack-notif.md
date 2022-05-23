### **Slack + Github**

Link Slack with github account following these images:

![app](../img/jenkins-pipe/slack/app.png)
![gh-app](../img/jenkins-pipe/slack/gh-app.png)
![connect github](../img/jenkins-pipe/slack/connect-gh.png)
![code](../img/jenkins-pipe/slack/code.png)

___
![auth](../img/jenkins-pipe/slack/auth.png)
![connect](../img/jenkins-pipe/slack/connect.png)
![free](../img/jenkins-pipe/slack/free.png)
![install](../img/jenkins-pipe/slack/install.png)
![plan](../img/jenkins-pipe/slack/plan.png)
![open](../img/jenkins-pipe/slack/open.png)

___

### **Jenkins + Slack**

1. Create Slack channel to receive the notifications once a build in Jenkins finish.
2. App > Jenkins > Add >. Configuration
![app jenkins](../img/jenkins-pipe/slack/app-jenkins.png)
![add](../img/jenkins-pipe/slack/add.png)
![link channel](../img/jenkins-pipe/slack/link-channel.png)
![instructions](../img/jenkins-pipe/slack/instructions.png)
![settings](../img/jenkins-pipe/slack/settings.png)
![slack-jenkins](../img/jenkins-pipe/slack/slack-jenk.png)
![secret](../img/jenkins-pipe/slack/secret.png)
___

### **Jenkinsfile**

    post {
        success {
            echo 'success!'
            slackSend color: "#11cd4b", channel: "#sqa-challenge-fabianpg-notif", message: "*Build Passed*\n Job: ${env.JOB_NAME}\n Build: ${env.BUILD_NUMBER}\n URL: ${env.BUILD_URL}"
        }
        failure {
            echo 'marked as failure'
            slackSend color: "#F50407", channel: "#sqa-challenge-fabianpg-notif", message: "*Build Failed*\n Job: ${env.JOB_NAME}\n Build: ${env.BUILD_NUMBER}\n URL: ${env.BUILD_URL}"
        }
        unstable {
            echo 'marked as unstable'
            slackSend color: "#df6805", channel: "#sqa-challenge-fabianpg-notif", message: "*Build Unstable*\n Job: ${env.JOB_NAME}\n Build: ${env.BUILD_NUMBER}\n URL: ${env.BUILD_URL}"
        }
        aborted {
            echo 'aborted'
            slackSend color: "#f3f024", channel: "#sqa-challenge-fabianpg-notif", message: "*Build Aborted*\n Job: ${env.JOB_NAME}\n Build: ${env.BUILD_NUMBER}\n URL: ${env.BUILD_URL}"        
        }
    }
___

### **results**

![builds](../img/jenkins-pipe/slack/builds.png)

![slack results](../img/jenkins-pipe/slack/slack-results.png)
