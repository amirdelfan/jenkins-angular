#!groovy

/* groovylint-disable-next-line CompileStatic */
pipeline {
  agent any

  tools { nodejs 'NODEJS' }

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
