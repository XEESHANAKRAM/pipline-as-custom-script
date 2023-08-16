pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''ls
pwd
echo "Hello"'''
      }
    }

    stage('Deploy Test') {
      parallel {
        stage('Deploy Test') {
          steps {
            echo 'Working Perfect'
          }
        }

        stage('QC') {
          steps {
            echo 'Code Test'
            sleep 10
          }
        }

      }
    }

    stage('Deploy-Prod') {
      steps {
        git(url: 'https://github.com/XEESHANAKRAM/jenkinsfile.git', branch: 'main')
      }
    }

  }
}