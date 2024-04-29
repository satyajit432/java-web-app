node{
    stage('checkoutcode'){
        git branch:'main', url:'https://github.com/satyajit432/java-web-app.git'
    }
    stage('buildcode'){
        sh '/opt/maven/bin/mvn clean package'
    }
    stage('deploytotomcat'){
        deploy adapters:[tomcat9(url:'http://13.200.250.59:8080/', credentialsId:'tomcatcred')], war:'**/*.war'
    }
}
