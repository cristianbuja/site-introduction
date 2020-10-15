pipeline {
  agent none
  stages {
    stage('Composer') {
      parallel {
        stage('PHP 7.3') {
          agent {
            docker {
              args '-v $HOME/.composer/cache:/.composer/cache'
              image 'typo3gmbh/php73'
            }

          }
          steps {
            sh 'php -v'
            sh 'composer install'
            sh 'composer validate'
          }
        }

        stage('PHP 7.2') {
          agent {
            docker {
              image 'typo3gmbh/php72'
              args '-v $HOME/.composer/cache:/.composer/cache'
            }

          }
          steps {
            sh 'php -v'
            sh 'composer install'
            sh 'composer validate'
          }
        }

      }
    }

  }
}