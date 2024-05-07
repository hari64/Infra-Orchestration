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
                sh 'sudo cp app.py /home/vagrant/staging/'
                
                // Restart your Python application on the same VM (if needed)
                sh 'sudo systemctl restart your-python-service'
            }
        }
    }
}
