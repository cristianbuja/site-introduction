pipeline {
  agent none
  stages {
    stage('Composer (PHP 7.3)') {
      parallel {
        stage('Composer (PHP 7.3)') {
          agent {
            docker {
              args '-v $HOME/.composer/cache:/.composer/cache'
              image 'typo3gmbh/php73'
            }

          }
          steps {
            sh 'composer install'
            sh 'composer validate'
          }
        }

        stage('Composer (PHP 7.2)') {
          agent {
            docker {
              image 'typo3gmbh/php72'
              args '-v $HOME/.composer/cache:/.composer/cache'
            }

          }
          steps {
            sh 'composer install'
            sh 'composer validate'
          }
        }

      }
    }

  }
}