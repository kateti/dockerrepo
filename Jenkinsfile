pipeline {
        agent { label 'centos' }

        stages {
                stage('create image') {
                        steps {
                                sh 'docker build -t ohurassa/pipeimage .'
                        }
                
                     }
               stage('create container') {
                        steps {
                                sh 'docker run -dit --name urassa ohurassa/pipeimage'
                        }
                
                     }
                }
       }
