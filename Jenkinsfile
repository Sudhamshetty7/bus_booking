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
                sh 'mvn --version'
                sh 'mvn clean install'
            }
        } 
    stage('deploy') {
             steps {
                 sh 'scp /home/slave-1/workspaceweather-update/_develop/target/bus-booking-app-1.0-SNAPSHOT.jar root@172.31.5.133:/opt/apache-tomcat-8.5.98/webapps/'
}
} 
    }
}
