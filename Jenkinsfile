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
              sh " "
            }
        }        
    }
}
