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
                sh 'docker run -d -p 8081:80 devops-lab-image'
            }
        }
    }
}
