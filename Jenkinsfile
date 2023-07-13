#!groovy

/* groovylint-disable-next-line CompileStatic */
pipeline {
  agent { dockerfile true }

  // agent {
  //   docker { image 'node:18.16.0-alpine' }
  // }

  // tools { nodejs 'NODEJS' }

  stages {
    stage('npm install and build') {
      steps {
        sh '''
          npm install -g @angular/cli
          npm install
          ng build -c production
        '''
      }
    }
  }
}
