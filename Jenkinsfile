pipeline {
  agent any
  stages {
    stage('Clone Repo') {
      steps {
        git credentialsId: 'github-creds', url: 'https://github.com/Anvesh7099/my-web-app.git', branch: 'main'
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

