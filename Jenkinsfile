#!groovy

/* groovylint-disable-next-line CompileStatic */
pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile'
      args '-u 0:0'
    }
  }

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
