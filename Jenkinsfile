pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Compile the .cpp file using shell script
                script {
                    sh 'g++ -o my_program Harshith_Reddy_C PES1UG22CS809.cpp'
                }
            }
        }
        
        stage('Test') {
            steps {
                // Print output of .cpp file using shell script
                script {
                    sh './my_program'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                // Deployment steps (if any)
                echo 'Deployment steps...'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
