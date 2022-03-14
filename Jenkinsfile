pipeline {
    agent any

    environment{
        PATH = "/opt/maven3/bin:$PATH"
    }
    stages{
        stage("Git Checkout"){
            steps{
                git branch: 'main', url: 'https://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@github.com/tamilarasanaccet30/Jenkins_CICD.git'
            }
        }
        stage("Maven Build"){
            steps{
                sh "mvn clean package"
             }
        }
    }
}
