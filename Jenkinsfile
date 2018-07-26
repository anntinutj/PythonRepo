pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'hai'
            sh 'echo "Hello World"'
            sh 'python pgm.pi'
          }
        }
        stage('Git Check') {
          steps {
            git(url: 'https://github.com/anntinutj/PythonRepo', branch: 'master', changelog: true, poll: true, credentialsId: 'anntinutj/3012@anila')
          }
        }
      }
    }
  }
}