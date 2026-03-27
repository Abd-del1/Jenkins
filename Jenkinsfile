pipeline {
    agent any

    stages {
        stage("Install Dependencies") {
            steps {
                dir("my-app") {
                    sh "npm install"
                }
            }
        }

        stage("Build") {
            steps {
                dir("my-app") {
                    sh "npm run build"
                }
            }
        }
    }

    post {
        always {
            echo "========always========"
        }
        success {
            echo "========A executed successfully========"
        }
        failure {
            echo "========A execution failed========"
        }
    }
}
