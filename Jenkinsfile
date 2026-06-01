pipeline {
  agent any

  environment {
    DOCKER_IMAGE = "YOUR_DOCKERHUB_USERNAME/my-cicd-app"
  }

  stages {

    stage('Clone') {
      steps {
        git branch: 'main',
        url: 'https://github.com/YOUR_USERNAME/my-cicd-app.git'
      }
    }

    stage('Build Docker Image') {
      steps {
        sh "docker build -t ${DOCKER_IMAGE}:${BUILD_NUMBER} ."
      }
    }

    stage('Push to DockerHub') {
      steps {
        withCredentials([usernamePassword(
          credentialsId: 'dockerhub-creds',
          usernameVariable: 'DOCKER_USER',
          passwordVariable: 'DOCKER_PASS'
        )]) {
          sh "echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin"
          sh "docker push ${DOCKER_IMAGE}:${BUILD_NUMBER}"
        }
      }
    }

    stage('Deploy') {
      steps {
        sh "docker run -d -p 80:3000 ${DOCKER_IMAGE}:${BUILD_NUMBER}"
      }
    }
  }

  post {
    success {
      echo 'Pipeline succeeded! App deployed.'
    }
    failure {
      echo 'Pipeline failed. Check logs.'
    }
  }
}pipeline {
  agent any

  environment {
    DOCKER_IMAGE = "YOUR_DOCKERHUB_USERNAME/my-cicd-app"
  }

  stages {

    stage('Clone') {
      steps {
        git branch: 'main',
        url: 'https://github.com/YOUR_USERNAME/my-cicd-app.git'
      }
    }

    stage('Build Docker Image') {
      steps {
        sh "docker build -t ${DOCKER_IMAGE}:${BUILD_NUMBER} ."
      }
    }

    stage('Push to DockerHub') {
      steps {
        withCredentials([usernamePassword(
          credentialsId: 'dockerhub-creds',
          usernameVariable: 'DOCKER_USER',
          passwordVariable: 'DOCKER_PASS'
        )]) {
          sh "echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin"
          sh "docker push ${DOCKER_IMAGE}:${BUILD_NUMBER}"
        }
      }
    }

    stage('Deploy') {
      steps {
        sh "docker run -d -p 80:3000 ${DOCKER_IMAGE}:${BUILD_NUMBER}"
      }
    }
  }

  post {
    success {
      echo 'Pipeline succeeded! App deployed.'
    }
    failure {
      echo 'Pipeline failed. Check logs.'
    }
  }
}
