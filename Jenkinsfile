pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "your-dockerhub-username/my-cicd-app"
    }

    stages {

        stage('Clone') {
            steps {
                git branch: 'main',
    url: 'https://github.com/DEEPAKMISAL01/devops-cicd-pipeline-aws.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-cicd-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 3000:3000 my-cicd-app || true'
            }
        }
    }

    post {
        success {
            echo 'Pipeline SUCCESS 🚀'
        }
        failure {
            echo 'Pipeline FAILED ❌'
        }
    }
}
