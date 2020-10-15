pipeline {
  agent {
    docker {
      image 'typo3gmbh/php73'
      args 'composer install'
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