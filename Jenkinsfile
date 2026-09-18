pipeline {
    agent any
    stages {
        stage('Build') {
            steps { echo 'building' }
        }
        stage('Tests') {
            parallel {
                stage('unit') { steps { sh 'echo unit tests' }}
                stage('Integration') { steps { sh 'echo integration tests' }}
            }
        }
    }
}   
