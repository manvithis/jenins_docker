pipeline {
    agent docker 
    stages {
        stage('git pull') {
            steps {
                checkout scm   
                }
        }
        stage('Example Test') {
            steps {
                echo 'unit test'
                
            }  
        }
        stage('Build dockerfile') {
            steps {
                sh 'docker build -t mytag .'
                
            }
    }
        stage('dockerfile Testing') {
            steps {
                sh 'docker run -d -p 80:80 mytag'
                echo "testing"
            }
        }
         stage('docker repository save==dockerhub/ECR') {
            steps {
                sh 'docker run -d -p 80:80 mytag'
  
            }
        }
}
}
