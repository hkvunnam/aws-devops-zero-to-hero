pipeline {
  agent none
  stages {
    stage('Back-end') {
      agent {
        docker { image 'openjdk:17' }
      }
      steps {
        sh 'java --version'
        sh 'hello-world.java'
      }
    }
    stage('Front-end') {
      agent {
        docker { image 'node:16-alpine' }
      }
      steps {
        sh 'node --version'
        sh 'node app.js'
      }
    }
  }
}
