pipeline {
  agent any
  
  stages {
    stage('Checkout') {
      steps {
        // Clonar el repositorio
        git 'https://github.com/PabelH/fullstack-app.git'
      }
    }
    
    stage('Build') {
      steps {
        // Acceder a la carpeta 'site'
        dir('site') {
          // Instalar dependencias con Yarn
          sh 'yarn install'
          
          // Construir la aplicación
          sh 'yarn build'
        }
      }
    }
  }
}