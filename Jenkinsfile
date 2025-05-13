pipeline {
    agent any
    stages {
        stage('Checkout Repo') {
            steps {
                sh '''
                    git clone https://github.com/kwapong91/devops-journal.git
                    git checkout may1-log
              '''
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
