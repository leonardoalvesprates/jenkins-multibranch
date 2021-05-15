pipeline {

  environment {
  }

  agent any
  
  stages {

    // ======================================================================main
    stage("[main] - echo") {
      when {
        branch 'main'
      }
      steps {
        sh label: '', script: ''' echo "this is main branch"
                                  echo'''
      }
    }

    stage("[main] - list dir") {
      when {
        branch 'main'
      }
      steps {
        sh label: '', script: ''' echo "recursive list directory"
                                  ls -lR'''
      }
    }

  }
}
