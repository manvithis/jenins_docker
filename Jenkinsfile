pipeline {
    agent any 
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
                sh 'sudo docker build –t=”mywebserver” .'
                
            }
    }
}







