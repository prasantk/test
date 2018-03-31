pipeline {
    agent {
        label 'docker-agent'
    }
    environment {
        shortCommit = sh(returnStdout: true, script: "git log -n 1 --pretty=format:'%h'").trim()
        tag = "${env.BUILD_NUMBER}_${shortCommit}"
    }
    stages {
        stage('print') {
            steps {
                sh "echo ${env.tag}"
            }
        }
    }
}