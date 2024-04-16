// input
https://www.jenkins.io/doc/book/pipeline/syntax/#input

pipeline {
    agent any 
    stages {
        stage ('Build') {
            steps {
                echo "Building the app"
            }
        }
        stage ('Test') {
            steps {
                echo "testing the app"
            }
        }
        stage ('DeployToDev') {
            steps {
                echo "Deploying to Dev env"
            }
        }
        stage ('DeployToProd') {
            steps {
                timeout (time: 300, unit: 'SECONDS') {
                     input message: 'Would you like to Promote to prod ??', ok: 'yes', submitter: 'maha'
                }
                echo "Deploying the app to Production"
            }
        }
    }
}
