pipeline {
    agent none
    stages {
        stage('Functional regression tests') {
            agent { docker {
                image 'ppodgorsek/robot-framework:latest'
                }
            }
            steps {
                sh '''
                    robot --version
                '''
            }
        }
    }
}
