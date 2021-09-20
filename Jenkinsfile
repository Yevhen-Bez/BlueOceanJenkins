pipeline {
  agent any
  stages {
    stage('checkoutGit') {
      steps {
        git(url: 'https://github.com/elestopadov/jenkins-example-app.git', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        echo 'My build'
      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            sleep 30
            echo 'Woow'
          }
        }

        stage('Deploy1') {
          steps {
            sleep 15
            echo 'Ohhh my'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Testing .....'
      }
    }

  }
}