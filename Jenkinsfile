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
    stage('testing') {
      steps {
        sh 'npm run test'
        input(message: 'Authoriza', submitter: 'developer')
        emailext(subject: 'Aprueba McAnnas', body: 'Aprueba', attachLog: true, replyTo: 'mauro.lozano@beone.mx', to: 'mauro.lozano@beone.mx')
      }
    }
  }
}