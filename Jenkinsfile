pipeline {
    agent any
    parameters {
        string(name: 'VERSION', defaultValue: '1.0', description: 'Version to deploy')
        choice(name: 'ENVIRONMENT', choices: ['staging', 'production'], description: 'Target')
        booleanParam(name: 'SKIP_TESTS', defaultValue: false, description: false, description: 'Skip teaser?')
    }
    stages {
        stage('Build') {
            steps {
                echo 'building'
            }
        }
    }
}   
