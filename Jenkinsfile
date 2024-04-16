// Parameters
// https://www.jenkins.io/doc/book/pipeline/syntax/#parameters
pipeline {
    agent any
    parameters {
        string(name: 'NAME', defaultValue: 'Siva' , description: 'Name of the Person' )
        text(name: "PARA", defaultValue: '', description: 'Enter highlevel fixes for the release')
        choice(name: 'ENV', choices: ['dev', 'Test', 'Prod'] , description: "Which Env would you like to deploy")
        booleanParam(name: 'TOOGLE', defaultValue: true, description: "Would you like to scan")
        password(name: 'SECRET', defaultValue: 'SECUREPASSWORD', description: "Enter the Password")
    } 
    stages {
        stage ('ParametesExample') {
            steps {
                echo "Welcome ${params.NAME}"
                echo "Fixes done are: ${params.PARA}"
                echo "Deploying to ${params.ENV}"
                echo "Are scans happening:${params.TOOGLE}"
                echo "The password enterd is: ${params.SECRET}"

            }
        }
    }
}
