pipeline {
    agent { label 'nithin' }
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
              sh "cp /home/nithin-slave/workspace/hello_pipe/target/hello-world-war-1.0.0.war  /opt/apache-tomcat-9.0.60/webapps"
            }
        }        
    }
}
