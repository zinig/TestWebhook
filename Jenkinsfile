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
            echo ${workspace}
           // steps {
           //     bat "dotnet restore ${workspace}\\C:\TestWebHook\TestWebhook\JenkinsConsole\\JenkinsConsole.sln"
        //}
        }
    }
}