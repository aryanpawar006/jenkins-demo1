pipeline {
    agent any
    parameters {
        choice(name: 'ENVIRONMENT', choices: ['staging', 'production'], description: 'target')
    }
    stages {
        stage('Build') { steps { sh 'echo Building' }}
        stage('Tests') {
            parallel {
                stage('unit') { steps { sh 'echo unit tests' }}
                stage('integration') { steps { sh 'echo integration tests' }}
            }
        }
        stage('Approve') {
            when { expression { params.ENVIRONMENT == 'production' }}
            steps { input message: 'Deploy to production?' }
        }
        stage('Deploy') { steps { sh "echo deploying to ${params.ENVIRONMENT}" }}
    }
}    
        
