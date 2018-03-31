pipeline {
    agent {
        label 'docker-agent'
    }
    environment {
        tag = ${env.BUILD_NUMBER} + '_' + sh(returnStdout: true, script: "git log -n 1 --pretty=format:'%h'").trim()
    }
    stages {
        stage('print') {
            steps {
                sh "echo ${env.tag}"
            }
        }
    }
}