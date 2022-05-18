pipeline{
      agent any
      stages{
      stage('check out'){
                  steps{
                  sh "rm -rf hello-world-war"
                  sh "git clone https://github.com/nithinbn1/hello-world-war.git"
                  }
                  }
      stage('build'){
      steps{
      sh "pwd"
      sh "ls"
      sh "cd hello-world-war"
      sh "docker build -t nithin412/dockimage:1.1 . "
      }
      }
       stage('publish'){
                  steps{
                        sh "docker login -u nithin412 -p nithinBn@07"
                        sh "docker push nithin412/dockimage:1.1"
                  }
            }
            stage('deploy'){
                  agent any
                  steps{
                        sh "docker login -u nithin412 -p nithinBn@07"
                        sh "docker pull nithin412/dockimage:1.0"
                        sh "docker rm -f trail1"
                        sh "docker run -d -p 8050:8080 --name trail1 nithin412/dockimage:1.1"
                  }
            }
      }
      }

