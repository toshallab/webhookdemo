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
            withCredentials([string(credentialsId: 'f3ced420-1776-4414-84af-ea548001c759', variable: 'mysecretvariable')]) {
                // some block
                echo mysecretvariable
        }
            sh 'npm install'    
            }
        }
    }
}