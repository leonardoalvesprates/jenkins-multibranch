pipeline {
    environment {
        MESSAGE = 'hello Hello HELLO'
    }
    agent any
    stages {
        stage('test main') {
            when {
              branch 'main'
            }
            steps {
               echo ${MESSAGE}
            }
        }
    }
}
