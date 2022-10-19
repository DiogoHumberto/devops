pipeline {
    agent any
    tools {
        maven 'Maven 3.8.6'
        jdk 'Java 1.8'
    }
    stages{
        stage ('Build do Projeto') {
            steps {
                sh '''
                    cd springProject
                    export MAVEN_HOME=/opt/maven
                    export PATH=$PATH:$MAVEN_HOME/bin
                    mvn --version
                    mvn clean package -DskipTests
                '''
            }
        }
    }
}