pipeline {
  agent any
  
  stages {
    stage('Clone repository') {
      steps {
        git 'https://github.com/PabelH/fullstack-app.git'
      }
    }
    
    stage('Build client') {
      steps {
        dir('site') {
          sh 'npm install'
          sh 'yarn build'
        }
      }
    }
    
    stage('Build and test server') {
      steps {
        dir('site') {
          sh 'npm install'
          sh 'yarn test'
        }
      }
    }
  }
}
