pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/imahalla/WebApp', branch: 'nain')
      }
    }

    stage('build') {
      steps {
        sh 'docker build -t webapp:latest . '
      }
    }

  }
}