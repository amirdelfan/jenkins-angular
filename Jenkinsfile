#!groovy

/* groovylint-disable-next-line CompileStatic */
pipeline {
  agent {
    dockerfile true
    args '-u root:root'
  }

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
