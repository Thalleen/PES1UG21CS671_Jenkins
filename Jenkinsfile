pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'PES1UG21CS671-1'
                    // Compile the .cpp file using shell script
                    sh 'g++ /main/test.cpp -o output'
                    
                    
                    
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    // Print the output of the .cpp file using shell script
                    sh './output'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                // Add deployment steps here if necessary
                echo 'deploy'
            }
        }
    }
    
    post {
        failure {
            // Display 'pipeline failed' in case of any errors within the pipeline
            echo 'pipeline failed'
        }
    }
}
