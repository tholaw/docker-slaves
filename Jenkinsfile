pipeline {
    agent none
    stages {
        stage('Functional regression tests') {
            agent { docker {
                image 'ppodgorsek/robot-framework:latest'
                args '--shm-size=1g -u root -v /var/jenkins_home/z-robot/tests:/opt/robotframework/tests -v /var/jenkins_home/z-robot/reports:/opt/robotframework/reports' }
            }
            environment {
                BROWSER = 'firefox'
                ROBOT_TESTS_DIR = "$WORKSPACE/robot-tests"
                ROBOT_REPORTS_DIR = "$WORKSPACE/robot-reports"
            }
            steps {
                sh '''
                    /opt/robotframework/bin/run-tests-in-virtual-screen.sh
                '''
            }
        }
    }
}
