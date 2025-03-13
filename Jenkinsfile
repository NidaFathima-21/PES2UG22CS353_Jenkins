pipeline {
    agent any  // Runs pipeline on any available agent

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ hello.cpp -o PES2UG22CS353'  // Compile the C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS353'  // Run the compiled executable
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...'  // Simulated deployment step
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'  // Display failure message if any stage fails
        }
    }
}
