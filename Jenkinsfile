pipeline {
  agent any
  stages {
    stage('git checkout') {
      parallel {
        stage('git checkout') {
          steps {
            git(url: 'https://github.com/ajay5844/simple-java-maven-app.git', branch: 'master', poll: true, credentialsId: 'Ajay@5844')
            bat(script: 'hello world', returnStdout: true, label: 'noway')
          }
        }

        stage('error') {
          steps {
            echo 'echo "happy"'
          }
        }

      }
    }

  }
}