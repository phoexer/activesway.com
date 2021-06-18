pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'npm install --global yarn'
                sh 'yarn'
            }
        }
        stage('Test') {
            steps {
                sh 'yarn test'
            }
        }
    }
}
