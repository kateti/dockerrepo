pipeline {
        agent any
        stages {
                stage('create image') {
                     agent { label 'centos' }
                        steps {
                                sh 'docker build -t ohurassa/pipeimage .'
                        }
                
                     }
               stage('create container') {
                       agent { label 'pull' }
                       steps {
                                sh 'docker run -dit --name urassa ohurassa/pipeimage'
                        }
                
                     }
                }
       }
