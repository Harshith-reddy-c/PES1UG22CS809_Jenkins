pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Since you're calling another Jenkins job 'PES1UG22CS809-1', use 'build' step to trigger it
                build job: 'PES1UG22CS809-1', wait: true // 'wait: true' ensures that this pipeline waits for the completion of the triggered job
                sh 'g++ main.cpp -o output' // Compile the code using g++
            }
        }
        stage('Test') {
            steps {
                sh './output' // Execute the compiled program
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...' // Corrected 'ech' to 'echo'
            }
        }
    }

    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
