pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                git url: 'https://github.com/Faluwi/msapp'
                sh "echo 'Build done.'"
            }
        }
        stage('Test') {
            steps {
                sh "echo 'Test done.'"
            }
        }
    }
}