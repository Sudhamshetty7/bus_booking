@Library('library-demo') _


pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    sh("""
                       git clone https://github.com/Sudhamshetty7/bus_booking.git
                       ls -ltr
                    """)
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    build 'install'
                }
            }
        }
    }
}
