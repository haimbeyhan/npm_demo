pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''npm install
npm run build'''
      }
    }
  }
  parameters {
    choice(name: 'REQUESTED_ACTION', choices: '''Build
''', description: 'Type of action to perform')
  }
}