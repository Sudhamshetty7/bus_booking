@Library('library-demo')
pipeline {
    agent { label 'node1' }
    stages {
        stage('checkout') {
            steps {
                sh 'git clone https://github.com/Sudhamshetty7/bus_booking'
            }
        }
        stage('build') {
            steps {
                build 'install'
            }
        }
    }
}

