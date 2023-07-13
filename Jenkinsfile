#!groovy

/* groovylint-disable-next-line CompileStatic */
pipeline {
  agent {
        docker {
      image 'node:6-alpine'
      args '-p 3000:3000 -p 5000:5000'
      args '-u 0:0'
        }
  }
    environment {
        CI = 'true'
    }

  // agent { dockerfile true  }

  // environment {
  //   // Override HOME to WORKSPACE value
  //   HOME = "${WORKSPACE}"
  //   // or override npm's cache directory (~/.npm)
  //   NPM_CONFIG_CACHE = "${WORKSPACE}/.npm"
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
