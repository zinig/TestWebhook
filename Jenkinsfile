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
                git branch: 'master', credentialsId: '4ba3aa74-75ee-46ac-91a4-a05901ff7e38', url: 'https://github.com/zinig/TestWebhook.git'
            }
        }
    }
}