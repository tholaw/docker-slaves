pipeline {
    agent {
        label 'robot-slave'
    }
    stages {
        stage('Functional regression tests') {
            steps {
                sh "docker run --shm-size=1g -e BROWSER=firefox -v /home/es018533/docker/robotfw-slave/robot:/opt/robotframework/tests:Z -v /home/es018533/docker/robotframework/reports:/opt/robotframework/reports:Z ppodgorsek/robot-framework:latest"
            }
        }
    }
}
