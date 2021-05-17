pipeline {
    environment {
        MESSAGE = 'hello Hello HELLO'
    }
    agent any
    stages {
        stage('echo message') {
            when {
              branch 'main'
            }
            steps {
               echo "${MESSAGE}"
            }
        }
        stage('build docker image') {
           when {
               branch 'main'
           }
           steps {
               script {
                   docker.build(webfirst, " . -f Dockerfile")
               }
           }
        }
    }
}
