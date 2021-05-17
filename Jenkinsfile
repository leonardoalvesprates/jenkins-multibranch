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
    }
}
