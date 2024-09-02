pipeline {
  agent any
  stages {
    stage('pull code fom github') {
      steps {
        git(url: 'https://github.com/Deep0409/Todo-list.git', branch: 'master')
      }
    }

    stage('Build') {
      steps {
        sh '''pwd
        echo "Building"'''
        sh ' sudo apt install apache2'
        sh 'echo "setup complete" '
      }
    }

    stage('Deploy') {
      steps {
   sh ' sudo mkdir -p /var/www/html'
   sh ' sudo cp -r ./* /var/www/html/'      
   sh ' sudo systemctl restart apache2'
      }
    }

  }
}
