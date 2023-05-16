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
        dir('site') {
          sh 'yarn install'
          sh 'yarn run test'
        }
      }
    }
    
    stage('Construir y probar frontend') {
      steps {
        dir('site') {
          sh 'yarn install'
          sh 'yarn run test'
        }
      }
    }
  }
}
