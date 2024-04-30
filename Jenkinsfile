pipeline {
    agent {
        node {
          Lable[jenkins-slave-node1-lable]
        }   
    }
    stages {
        stage('checkoutcode') {
            steps{
                git branch: 'main' , url:'https://github.com/satyajit432/java-web-app.git'
            } 
        }
        stage('buildcode') {
            steps{
                sh '/opt/maven/bin/mvn clean package'
            }
        }
    }
}