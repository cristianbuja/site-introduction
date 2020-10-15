pipeline {
  agent {
    docker {
      image 'typo3gmbh/php73'
    }

  }
  stages {
    stage('Composer') {
      steps {
        sh 'composer install'
      }
    }

  }
}