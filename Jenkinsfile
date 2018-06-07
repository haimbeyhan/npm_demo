pipeline {
  agent any
  stages {
    stage('Build Demo App') {
      when {
        expression {
          params.REQUESTED_ACTION == 'Build'
        }

      }
      steps {
        sh '''npm build
npm run build'''
        sh '''npm install
npm run build'''
      }
    }
    stage('Test') {
      steps {
        sh 'npm run test'
      }
    }
  }
  parameters {
    choice(name: 'REQUESTED_ACTION', choices: '''Build
''', description: 'Type of action to perform')
  }
}