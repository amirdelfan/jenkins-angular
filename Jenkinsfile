#!groovy

/* groovylint-disable-next-line CompileStatic */
pipeline {
  agent { dockerfile true  }

  environment {
    // Override HOME to WORKSPACE value
    HOME = "${WORKSPACE}"
    // or override npm's cache directory (~/.npm)
    NPM_CONFIG_CACHE = "${WORKSPACE}/.npm"
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
