pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
     
    stage('Test') {
      steps {
         sh 'npm test'
      }
    }

    stage('Publish Report') {
        publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'unit-test-results', reportFiles: 'mochawesome.html', reportName: 'Mochawesome Unit Test Report', reportTitles: ''])
    }    
  }
}