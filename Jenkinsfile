﻿pipeline {
    agent any
    stages {
        stage('Send Email') {
            steps {
        
                echo 'Send Email'
            }
        }
    }
    post {
        always { 
            echo 'I will always say Hello!'
        }
        aborted {
            echo 'I was aborted'
        }
        failure {
            mail to: 'sdhamdar9008@gmail.com',
            subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
            body: "Something is wrong with ${env.BUILD_URL}"
        }
    }
}
