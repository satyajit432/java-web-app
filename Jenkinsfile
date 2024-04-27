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
        stage('cicdpipeline') {
            steps {
                deploy adapters: [tomcat9(url:'http://3.110.159.249:8080/', credentialsId:'tomcatcred')], war: '**/*.war'
            }

        }
    }
}
