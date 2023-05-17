pipeline {
  agent any
  
    stages {
        stage('Clone repository') {
            steps {
               
                    git 'https://github.com/PabelH/fullstack-app.git' 
            }
        }
        stage('Install dependencies') {
            steps {
                dir('site') {
                sh 'curl --silent --location https://dl.yarnpkg.com/rpm/yarn.repo | sudo tee /etc/yum.repos.d/yarn.repo' // Instalar el repositorio de Yarn
                sh 'sudo yum install -y yarn' // Instalar Yarn
                sh 'yarn install' // Instalar las dependencias del proyecto 
                }
            }
        }
        stage('Run tests') {
            steps {
                dir('site') {
                    sh 'yarn test' 
                }
            }
        }
    }
}
