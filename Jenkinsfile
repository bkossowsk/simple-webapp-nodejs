pipeline {
    agent any

    stages {
        stage('CleanWS') {
            steps {
                cleanWs()
            }
        }
        stage('Clone') {
            steps {
                git 'https://github.com/bkossowsk/simple-webapp-nodejs.git'
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run tests') {
            steps {
                sh 'npm run test'
            }
        }
    }
}
