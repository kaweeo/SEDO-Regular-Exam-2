pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/kaweeo/SEDO-Regular-Exam-2.git'
            }
        }
        stage('Setup .NET') {
            steps {
                sh 'dotnet --version'
            }
        }
        stage('Restore') {
            steps {
                sh 'dotnet restore'
            }
        }
        stage('Build') {
            steps {
                sh 'dotnet build --no-restore'
            }
        }
        stage('Test') {
            steps {
                sh 'dotnet test'
            }
        }
    }
}
