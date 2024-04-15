//allOf

pipeline {
    agent any 
    environment {
        // our own custom env variables
        DEPLOY_TO = 'production'
    }
    stages {
        stage ('DepoyToDev') {
            steps {
                echo "Deploying to Dev Environment"
            }
        }
        stage ('ProdDeploy') {
            when {
                allOf {
                    branch 'production'
                    environment name: 'DEPLOY_TO', value: 'production'
                }

            }
            steps {
                echo "Deploying to production"
            }
        }
    }
}
