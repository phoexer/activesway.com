pipeline {
    agent {
        docker {
            image 'node:12.16.1'
        }
    }
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
    post {
        success {
            setBuildStatus("Build succeeded", "SUCCESS");
        }
        failure {
            setBuildStatus("Build failed", "FAILURE");
        }
      }
}
