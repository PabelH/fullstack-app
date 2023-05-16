pipeline {
  agent any
  
  stages {
    stage('Clonar repositorio') {
      steps {
        git 'https://github.com/PabelH/fullstack-app.git'
      }
    }
    
    stage('Construir y probar backend') {
      steps {
        dir('backend') {
          sh 'npm install'
          sh 'npm run test'
        }
      }
    }
    
    stage('Construir y probar frontend') {
      steps {
        dir('frontend') {
          sh 'npm install'
          sh 'npm run test'
        }
      }
    }
  }
}
