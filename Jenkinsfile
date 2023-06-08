pipeline {
	
    
    stages {
	stage('Create docker image') {
	   agent {label 'centos'}   /* creating the docker image. */
            steps {
                sh 'docker build -t testpipe'
            }
		post {
			success {
			   echo 'This pipeline tage ran without error!'
			}	
			failure {
				echo 'You need to review your code please!'
			}
		}
        }
        stage('Create docker container') {
            agent {label 'pull'}
            steps {
                sh 'docker run -dit --name ohurassa/testpipe'
            }
        }
    }

  }
	
