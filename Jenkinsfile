pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/hari64/Infra-Orchestration.git'
            }
        }
        stage('Build') {
            steps {
                sh 'vagrant up'
            }
        }
        stage('Test') {
            steps {
                // Add test steps if applicable
            }
        }
        stage('Deploy to Staging') {
            steps {
                sshagent(['jenkins']) {
                   sh 'ssh vagrant@infra.com "cd /path/to/deployment && vagrant up"'
                }
            }
        }
        stage('Smoke Test') {
            steps {
                // Add smoke test steps if applicable
            }
        }
    }

    post {
        success {
            echo 'CI/CD pipeline succeeded! Application deployed to staging environment.'
        }
        failure {
            echo 'CI/CD pipeline failed! Check Jenkins logs for details.'
        }
    }
}
