pipeline {
    agent { docker {
        image 'ppodgorsek/robot-framework:latest'
        args '--shm-size=1g -u root' }
        }
    stages {
        stage('Test') {
            steps {
                sh 'robot --version'
            }
        }
    }
}
