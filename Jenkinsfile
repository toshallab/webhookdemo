pipeline {
    agent any
    tools {nodejs "mynodejs"}

    stages {
        stage('Dev') {
            steps {
                git 'https://github.com/toshallab/webhookdemo.git/'
                echo "webhook  file content "
                sh 'cat webhook.txt'
            }
        }
        stage ('build') {
            steps {
            withCredentials([string(credentialsId: '2d6a38af-b122-47ef-bf72-54fc850ddb5e', variable: 'mysecret')]) {
                // some block
                echo mysecret
        }
            sh 'npm install'    
            }
        }
    }
}