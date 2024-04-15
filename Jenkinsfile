// based on the branch condition, i can create the pipeline
// BRANCH_NAME variable is only available in Multi Branch pipeline/Git hub or pipleines 

pipeline {
    agent any 
    environment {
        // our own custom env variables
        DEPLOY_TO = 'production'
    }
    stages {//allOf

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
        stage ('DepoyToDev') {
            steps {
                echo "Deploying to Dev Environment"
            }
        }
        stage ('ProdDeploy') {
            when {
                // brnach condition
                expression { BRANCH_NAME == /(production|staging)/ }
            }
            steps {
                echo "Deploying to production"
            }
        }
    }
}
