pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/harinip1509/git-lab-group5.git'
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
