pipeline {
    agent {
        label 'docker-agent'
    }
    environment {
        shortCommit = sh(returnStdout: true, script: "git log -n 1 --pretty=format:'%h'").trim()
    }
    stages {
        stage('print') {
            steps {
                sh "echo ${env.shortCommit}"
            }
        }
    }
}