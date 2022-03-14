pipeline {
    agent any
    
    stages {
           stage ('Build') {
            steps {
                bat 'mvn install package'
            }
        }
        stage('Deploy'){
            steps{
                deploy adapters: [tomcat8(credentialsId: '03178233-4ffc-4d6b-97f1-3767b9519a0e', path: '', url: 'http://localhost:9090/')], contextPath: null, war: '**/*.war'
            }
        }
    }
}
