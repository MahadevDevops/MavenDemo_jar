pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        echo 'checkout scm'
        mail(subject: 'blue ocean mail', body: 'blue ocean mail', to: 'mahadeva.garad1@gmail.com')
        git(url: 'https://github.com/MahadevDevops/MavenDemo_jar.git', branch: 'master', poll: true)
      }
    }
  }
}