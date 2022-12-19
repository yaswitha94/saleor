pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('vcs') {
            steps {
                git branch: 'main', url: 'https://github.com/yaswitha94/saleor.git'
        }
        stage('docker image build') {
            steps {
                sh 'docker image build -t yaswithaa/saleor:DEV .'
            }
        }
    }
}