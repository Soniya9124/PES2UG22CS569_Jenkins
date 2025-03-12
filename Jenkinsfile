pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building C++ project...'
                    sh 'g++ -o PES2UG22CS569-1 main.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running C++ program...'
                    sh './PES2UG22CS569-1'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Add deployment steps here
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
