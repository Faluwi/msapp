def gitPath = 'https://github.com/Faluwi/msapp'
def name = 'msapp'
pipeline {
    agent any
    stages {
        stage('Cleanup') {
            steps {
                script {
                    openshift.withCluster() {
                        openshift.withProject('dev') {
                            echo "Using Project: ${openshift.project()}"
                            if(openshift.selector("all", [app: name]).exists()) {
                                openshift.selector('all', [app : name]).delete()
                                echo "Old ressources deleted"
                            }
                        }
                    }
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    openshift.withCluster() {
                        openshift.withProject('dev') {
                            openshift.newApp('nodejs', gitPath)
                        }
                    }
                }
            }
        }
    }
}
