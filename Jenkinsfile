pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/imahalla/WebApp', branch: 'nain')
      }
    }

    stage('log') {
      steps {
        sh 'ls -la'
      }
    }

  }
}