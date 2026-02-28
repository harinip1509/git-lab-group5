pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-username/your-repo-name.git'
            }
        }

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
