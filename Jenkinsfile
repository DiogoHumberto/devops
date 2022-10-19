pipeline {
    agent any
    stages{
        stage ('Build do Projeto') {
            steps {
                sh '''
                    cd springProject
                    apt-get mvn install
                    mvn clean package -DskipTests
                '''
            }
        }
    }
}