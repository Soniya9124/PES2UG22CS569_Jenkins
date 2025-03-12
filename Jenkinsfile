pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                checkout([$class:'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[url: 'https://github.com/Soniya9124/PES2UG22CS569_Jenkins.git']]
                ])
            }
        }

        stage('Build') {
            steps {
                sh 'g++ main/hello.cpp -o main/output'
            }
        }

        stage('Test') {
            steps {
                sh './main/output'
            }
        }
        stage("Deploy'){
              steps {
                  echo 'deploy'
              }
        } 
    }
    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
