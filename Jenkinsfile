pipeline {
  agent any
  stages {
    stage('Clone Repo') {
      steps {
        git 'https://github.com/your-username/my-web-app.git'
      }
    }
    stage('Build Docker Image') {
      steps {
        sh 'docker build -t my-web-app .'
      }
    }
    stage('Run Container') {
      steps {
        sh 'docker run -d -p 8081:80 my-web-app'
      }
    }
  }
}

