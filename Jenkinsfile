pipeline {
    agent any
    stages {
        stage('CICD') {
            steps {
                script {
                    openshift.withCluster() {
                        openshift.withProject('') {
                            echo "Using Project: ${openshift.project()}"
                        }
                    }
                }
            }
        }
        stage('DEV') {
            steps {
                script {
                    openshift.withCluster() {
                        openshift.withProject('dev') {
                            echo "Using Project: ${openshift.project()}"
                        }
                    }
                }
            }
        }
        stage('PROD') {
            steps {
                script {
                    openshift.withCluster() {
                        openshift.withProject('prod') {
                            echo "Using Project: ${openshift.project()}"
                        }
                    }
                }
            }
        }
    }
}
