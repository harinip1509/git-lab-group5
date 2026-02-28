pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-lab-image .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker rm -f devops-container || true'
                sh 'docker run -d -p 8082:80 --name devops-container devops-lab-image'
            }
        }
    }
}
