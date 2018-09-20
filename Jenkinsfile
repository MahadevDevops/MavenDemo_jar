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
      steps {
        echo 'Im in build stage'
        sh 'mvn clean compile'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
  }
}