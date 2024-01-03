pipeline {
  agent any
  stages {
    stage('checkoutGit') {
      steps {
        git(url: 'https://github.com/elestopadov/java-example-apps.git', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        echo 'This is build'
      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy to Dev_1') {
          steps {
            echo '1'
          }
        }

        stage('Deploy to Dev_2') {
          steps {
            sleep 15
            echo '2'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Test'
      }
    }

  }
}