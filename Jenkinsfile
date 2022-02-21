pipeline {
  agent {
    docker {
      image 'node:12'
      args '--network tutorial_jenkins_mynet'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        sh 'npm run test -- --coverage --watchAll=false'
      }
    }

  }
}