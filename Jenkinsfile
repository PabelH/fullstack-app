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
                // Instalar dependencias y compilar
                sh 'npm install'
                sh 'yarn start'
            }
        }
        
        stage('Test') {
            steps {
                // Ejecutar pruebas
                sh 'yarn test'
            }
        }
    }
}
