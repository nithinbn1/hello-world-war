pipeline {
    agent any
    stages {
        stage('checkout') { 
            steps {
              sh "git clone https://github.com/nithinbn1/hello-world-war.git"
            }
        }
stage('build dockerfile') { 
            steps {
              sh "docker build -t tomcatprj ."
            }
        }         
     }
}


