//allOf

pipeline {
    agent any 
    environment {
        // our own custom env variables
        DEPLOY_TO = 'xyz'
    }
    stages {
        stage ('DepoyToDev') {
            steps {
                echo "Deploying to Dev Environment"
            }
        }
        stage ('ProdDeploy') {
            when {
                anyOf {
                    // 10 contions, then all the 10 conitions should be satisfied
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
