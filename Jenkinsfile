<<<<<<< HEAD
pipeline {
    agent any
    stages {
        stage('checkoutcode') {
            steps {
                git branch: main, url: 'https://github.com/satyajit432/java-web-app.git'
            }

        }
        stage('buildcode') {
            steps {
                sh '/opt/maven/bin/mvn clean package'
            }

        }
        stage('buildcode') {
            steps {
                deploy adapters: [tomcat9(url:'http://15.207.106.147:8080/', credentialsId:'tomcatcred')], war: '**/*.war'
            }

        }
    }
}
=======
pipeline{
    agent any
    stages {
        stage('checkoutcode'){
            steps{
                git branch: main, url: 'https://github.com/satyajit432/java-web-app.git'
            }

        }
        stage('buildcode'){
            steps{
                sh '/opt/maven/bin/mvn clean package'
            }

        }
        stage('cicdpipes'){
            steps{
                deploy adapters: [tomcat9(url:'http://15.207.106.147:8080/', credentialsId:'tomcatcred')], war: '**/*.war'
            }

        }
    }
}
>>>>>>> 58a168d934625b016aa81d9e6f4ff65746eeffb5
