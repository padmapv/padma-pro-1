pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        git(url: 'https://github.com/padmapv/padma-pro-1.git', branch: 'master', poll: true)
      }
    }
    stage('BUILD') {
      steps {
        sh 'mvn clean compile package'
      }
    }
    stage('DEPLOY') {
      steps {
        sh 'mvn deploy'
      }
    }
  }
}