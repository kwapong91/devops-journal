pipeline {
    agent any
    stages {
        stage('Checkout Repo') {
            steps {
                git branch: 'may1-log', url: 'https://github.com/kwapong91/devops-journal.git'
            }
        }
        stage('Run Python Script') {
            steps {
              sh 'python3 docker-practice/app.py'
            }
        }
        stage('Build Docker Image') {
            steps {
              sh 'docker build -t simple_application'
            }
        }      
    }
}
