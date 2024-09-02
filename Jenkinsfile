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
      }
    }

    stage('Deploy') {
      steps {
   sh 'echo "a" | sudo -S mkdir -p /var/www/html'
   sh 'echo "a" | sudo -S cp -r ./* /var/www/html/'      
   sh 'echo "a" | sudo -S systemctl restart apache2'
      }
    }

  }
}
