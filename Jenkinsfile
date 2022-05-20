pipeline {
  agent any
  stages {
    stage('scm') {
      steps {
        git 'https://github.com/rsivaseshu/sample-java.git'
      }
    }

    stage('Build') {
      steps {
        sh 'mvn -Dmaven.test.failure.ignore=true clean package'
      }
    }

  }
  tools {
    maven 'maven'
  }
}