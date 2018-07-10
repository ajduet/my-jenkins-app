pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'git pull origin master'
        sh 'mvn clean package'
      }
    }
  }
}