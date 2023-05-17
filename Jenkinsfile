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
                    sh 'curl --silent --location https://dl.yarnpkg.com/rpm/yarn.repo | sudo tee /etc/yum.repos.d/yarn.repo'
                    sh 'yarn install' 
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
