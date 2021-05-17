pipeline {
    environment {
        MESSAGE = 'hello Hello HELLO'
        DOCKER_IMAGE_NAME = 'webfirst'
        TAG_PRD = "prd-${BUILD_NUMER}"

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
                   env.IMAGE_NAME = "${DOCKER_IMAGE_NAME}:${TAG_PRD}"
                   DOCKER_IMAGE = docker.build(env.IMAGE_NAME, " . -f Dockerfile")
               }
           }
        }
    }
}
