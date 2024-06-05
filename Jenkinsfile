pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/31304/lab12.git'
            }
        }
        stage('Dependency Installation') {
            steps {
                bat 'npm install'
            }
        }
        stage('Build') {
            steps {
                bat 'docker build -t frontend .'
            }
        }
        stage('Run') {
            steps {
                bat 'docker start frontend'
            }
        }
        stage('Push') {
            steps {
                bat 'docker push frontend'
            }
        }
    }
}
