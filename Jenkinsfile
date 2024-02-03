pipeline {
    agent {label 'java'}
    stages {
        stage('Checkout') {
            steps {
                script {
                    sh 'git clone https://github.com/Sudhamshetty7/bus_booking.git'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    sh 'mvn clean install'
                }
            }
        }
    }
}
