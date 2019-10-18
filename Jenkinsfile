pipeline {
  agent any

  stages {
    stage('Install dep.') {
      steps {
        step {
          nodejs(nodeJSInstallationName: 'node10') {
            sh 'node -v'
            sh 'npm -v'
          }
        }
      }
    }
    stage('Run tests') {
      steps {
        step{
          sh 'npm install'
          sh 'npm test'          
        }

      }
    } 
    stage('Clean up') {
      steps{
        steps {
          sh 'ls -lA'
        }        
      }
    } 
  }
}