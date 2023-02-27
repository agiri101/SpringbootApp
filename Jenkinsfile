pipeline {
    agent any
    environment {
     BRANCH_NAME = "main"

  }
    stages{
        stage("clone code"){
            steps{
                echo "${env.BRANCH_NAME}"
                git credentialsId: '1e8a445e-5b4d-4c79-a8ce-c73cc1adfb65', url: 'https://github.com/agiri101/SpringbootApp.git'
            }
        }
        stage("build code"){
            steps{
                sh "mvn clean install"
            }
        }
    }
}