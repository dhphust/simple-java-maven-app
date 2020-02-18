pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'print'
      }
    }

    stage('test') {
      steps {
        unstable 'print test'
      }
    }

  }
}