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
        sh '''cp -r ./*.html /var/www/html/
        cp -r ./*.js /var/www/html/
        cp -r ./*.css /var/www/html/
systemctl restart apache2'''
      }
    }

  }
}
