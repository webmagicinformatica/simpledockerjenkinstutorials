pipeline {
    agent any
    parameters{
        string(name: 'image-name', defaultValue: 'dab8106/auricle')
    }
    stages {
        stage('Check Docker Installtion') {
            steps {
                sh 'docker info'
            }
        }
        stage('Pulling Image From Docker Hub') {
            steps {
                sh 'sh pull.sh'
            }
        }
        stage('Running Docker Image') {
            steps {
                sh 'sh run.sh'
            }
        }
    }
}
