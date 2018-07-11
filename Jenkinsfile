pipeline {
  agent any
  stages {
    stage('Install') {
      steps {
        sh 'npm install'
      }
    }
    stage('buid') {
      steps {
        sh 'npm run build'
      }
    }
  }
}