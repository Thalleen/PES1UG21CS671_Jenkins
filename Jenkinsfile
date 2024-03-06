pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using shell script
                    sh 'g++ -o output_file /main/test.cpp'
                    
                    // Build YOUR_SRN-1 (if necessary)
                    sh 'make PES1UG21CS671-1'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    // Print the output of the .cpp file using shell script
                    sh './output_file'
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
