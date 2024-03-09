pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Compile the .cpp file using shell script
                script {
                    sh 'g++ -o hello.cpp'
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
