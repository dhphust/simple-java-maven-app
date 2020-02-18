pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2:/root/.m2'
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
        echo 'this is a build'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'mvn test'
          }
        }

        stage('test1') {
          steps {
            echo 'this is a test1'
          }
        }

      }
    }

    stage('deliver') {
      steps {
        sh './jenkins/scripts/deliver.sh'
      }
    }

  }
}