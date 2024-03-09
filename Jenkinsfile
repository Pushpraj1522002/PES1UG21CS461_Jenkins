pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS461-1'    
                sh 'g++ main.cpp -o output'
            }
        }
        
        stage('Test') {
            steps {
                    sh './output_error'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    
    post {
        failure {
                error 'Pipeline failed'
            }
        }
    }

