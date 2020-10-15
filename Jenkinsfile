pipeline {
  agent {
    docker {
      image 'typo3gmbh/php73'
    }

  }
  stages {
    stage('Composer (PHP 7.3)') {
      steps {
        sh 'composer install'
        sh 'composer validate'
      }
    }

  }
}