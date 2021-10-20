pipeline {
    agent { docker {
        image 'ppodgorsek/robot-framework:latest'
        }
    }
    stages {
        stage('Functional regression tests') {
            steps {
                sh '''
                    robot --version
                '''
            }
        }
    }
}
