pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'python3 app.py'
            }
        }
        stage('Deploy to Staging') {
            steps {
                // Copying files to staging directory on the same VM
                sh 'rsync -av app.py /home/vagrant/staging/'
                
            }
        }
    }
}
