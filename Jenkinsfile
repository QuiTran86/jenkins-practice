pipeline {
    agent any
    options {
        lock resource: 'resource-lock'
        skipDefaultCheckout()
    }
    stages{
        stage('Clone Code') {
            steps{
                git 'https://github.com/QuiTran86/jenkins-practice.git'
            }
        }
        stage('Docker build image') {
            steps{
                sh 'docker build -t nginx-web:latest .'
            }
        }
        stage('Build') {
            steps{
                    echo "Build finished"
                    sleep 300


            }
        }

    }
}