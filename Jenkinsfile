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
