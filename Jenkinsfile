pipeline {
        agent any
        stages {
                /* stage('create image') {
                     agent { label 'centos' }
                        steps {
                                sh 'docker build -t ohurassa/pipeimage .'
                                sh 'docker login -u ohurassa -p ynpassword'
                                sh 'docker push ohurassa/pipeimage:v1'
                        }
                
                     } */
              stage('create container') {
                       agent { label 'pull' }
                      steps {
                                sh 'docker login -u ohurassa -p ynpassword'
                                sh 'docker pull ohurassa/pipeimage'
                                sh 'docker run -dit --name urassa ohurassa/pipeimage'
                        }
                
                     } 
                }
       }
