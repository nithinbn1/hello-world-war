pipeline {
    agent any
    stages {
        stage('checkout') { 
            steps {
              sh "git clone https://github.com/nithinbn1/hello-world-war.git"
            }
        }
stage('build') { 
            steps {
              sh "mvn clean package"
            }
        }         
        stage('deploy') { 
            steps {
              sh "cp /var/lib/jenkins/workspace/Hello_pipe/target/hello-world-war-1.0.1.war /opt/apache-tomcat-9.0.60/webapps/"
            }
        }         
    }
}


