pipeline{
    agent any
    tools {
  maven 'M2_HOME'
    }
    stages{
        stage("Code Checkout"){
            steps{
                git credentialsId: '8cd5225c-be14-49b6-9d25-1e2edc715d78', url: 'https://github.com/vasu7github/my-app.git'
            }
        }
        stage("BUILD"){
            steps{
                sh 'mvn clean install package'
            }
        }
        stage("Test"){
            steps{
                sh 'mvn test'
            }
        post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}    
