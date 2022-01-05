pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh "echo 'Build done.'"
            }
        }
        stage('Test') {
            steps {
                sh "echo 'Test done.'"
            }
        }
        stage('Deploy') {
            steps {
                script {
                    openshift.withCluster() {
                        openshift.withProject('dev') {
                            sh "echo ${openshift.project"
                    }
                }
                sh "echo 'Deploy done.'"
            }
        }
    }
}
