pipeline{
    agent any
    stages{
        stage("Checkout"){
            steps{
                git url: "https://github.com/Abd-del1/Jenkins.git"
            }
        stage("Install Dependencies"){
             steps{
                sh "npm install"
             }  
            }
        stage("Build"){
             steps{
                sh "npm run build"
             }  
            }
        post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
            }
        }
    }
}
