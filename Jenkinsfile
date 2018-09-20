pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        echo 'checkout scm'
        git(url: 'https://github.com/MahadevDevops/MavenDemo_jar.git', branch: 'master', poll: true)
      }
    }
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Im in build stage'
            sh 'mvn clean compile'
          }
        }
        stage('Build1') {
          steps {
            sleep(time: 1, unit: 'MILLISECONDS')
          }
        }
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
  }
}