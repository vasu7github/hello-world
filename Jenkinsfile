ppipeline{
    agent any
    stages{
        stage("SCM checkout"){
            steps{
                git changelog: false, poll: false, url: 'https://github.com/vasu7github/hello-world.git'
            }
        }
        stage("maven Build"){
            steps{
                bat "mvn clean package"
            }
        }
    }
}
