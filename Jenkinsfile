pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {

                    build 'PES1UG21CS671-1'
                    sh 'g++ test.cpp -o output'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                   
                    sh './output'
                }
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
            
            error 'pipeline failed'
        }
    }
}
