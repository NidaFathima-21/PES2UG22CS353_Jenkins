pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ new_hello.cpp -o PES2UG22CS353'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './WRONG_EXECUTABLE'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
