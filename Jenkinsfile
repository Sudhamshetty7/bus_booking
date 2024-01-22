pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    sh 'rm -rf bus_booking'
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
    
        stage("SonarQube analysis") {
            steps {
                script {
                withSonarQubeEnv('sonar') {
                sonar()    
            }
            }
        }
    }  
    }
}
