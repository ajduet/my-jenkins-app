pipeline {
  agent {
    docker {
      image: 'maven:3.6.3-openjdk-8-slim'
      args: '-v $HOME/.m2:/root/.m2'
    }
  }
  stages {
    stage('Info') {
      steps {
        sh 'mvn --version'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Build') {
      steps {
        sh 'mvn package -DskipTests'
      }
    }
  }
}