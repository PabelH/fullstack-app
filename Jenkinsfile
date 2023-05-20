pipeline {
  agent any
  
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/PabelH/fullstack-app.git'
      }
    }
    
    stage('Build') {
      steps {
        dir('site') {
          sh 'npm install'
          
          //sh 'yarn test'
        }
      }
    }
  }
}
