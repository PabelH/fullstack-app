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
                    sh 'npm i' 
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
