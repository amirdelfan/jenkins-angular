#!groovy

pipeline {
  agent any
 
  tools {nodejs "NODEJS"}
 
  stages {
    stage('Example') {
      steps {
        sh 'npm config ls'
      }
    }
  }
}