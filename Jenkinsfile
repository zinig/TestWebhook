pipeline {
    agent any
    stages {
        stage ('Clean workspace') {
            steps {
                cleanWs()
            }
        }
        stage ('Git Checkout') {
            steps {
                git branch: 'main', 
                credentialsId: '4ba3aa74-75ee-46ac-91a4-a05901ff7e38', 
                url: 'https://github.com/zinig/TestWebhook.git'
            }
        }
        stage('Restore packages') {
            steps {
                echo "${workspace}"
                bat "dotnet restore ${workspace}\\JenkinsConsole\\JenkinsConsole.sln"
            }
        }
    }
}