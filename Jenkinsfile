@Library('library-demo') _

pipeline {
    agent { label 'node1' }
    stages {
        stage('checkout') {
            steps {
                sh 'rm -rf bus_booking'
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

