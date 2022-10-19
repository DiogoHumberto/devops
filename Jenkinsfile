pipeline {
    agent any
    stages{
        stage ('Build do Projeto') {
            withMaven  {
                sh '''
                    cd springProject
                    mvn -version
                    mvn clean package -DskipTests
                '''
            }
        }
    }
}