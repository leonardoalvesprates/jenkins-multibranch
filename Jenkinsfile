pipeline {
    agent any
    stages {
        stage('test main') {
            when {
              branch 'develop'
            }
            steps {
               echo "hello" 
            }
        }
    }
}