pipeline {
  agent {
    docker {
      image 'maven:3.6.3-jdk-8'
    }

  }
  stages {
    stage('prep') {
      steps {
        sh '''echo hello world
'''
        echo 'Running File'
      }
    }

    stage('compile') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('package') {
      steps {
        sh 'mvn package'
      }
    }

    stage('archive') {
      steps {
        junit '**/*/.xml'
      }
    }

  }
  environment {
    USER_NAME = 'manpreet'
  }
}